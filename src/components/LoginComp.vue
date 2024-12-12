<template>
    <div class="login-form">
      <h1 class="login-title">Login</h1>
  
      <!-- Login Form -->
      <form @submit.prevent="handleLogin">
        <div class="form-group">
          <label for="username">Username</label>
          <input 
            type="text" 
            id="username" 
            v-model="username" 
            placeholder="Enter your username" 
            required
          />
        </div>
        
        <div class="form-group">
          <label for="password">Password</label>
          <input 
            type="password" 
            id="password" 
            v-model="password" 
            placeholder="Enter your password" 
            required
          />
        </div>
  
        <div class="form-actions">
          <button type="submit" class="login-btn">Login</button>
        </div>
        
        <div class="forgot-password">
          <p>Forgot password? <router-link to="/forgot-password"> Reset Password</router-link></p>
        </div>
      </form>
    </div>
</template>
  
<script>
  export default {
    name: 'LoginComponent',
    data() {
      return {
        username: 'user1',  // Example for username
        password: 'password123', // Example for password
      };
    },
    methods: {
      handleLogin() {
        if (this.username === 'user1' && this.password === 'password123') {
          // Username and password match, perform login logic 
          this.$router.push({ name: 'home' }); // Redirect to home page on success
        } else {
          alert('Invalid credentials'); // Display error message if credentials are incorrect
        }
      }
    }
  }
</script>
  
<style scoped>
  .login-form {
    background-color: #fff;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 400px;
  }
  
  .login-title {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 1.5rem;
  }
  
  .form-group {
    margin-bottom: 1.2rem;
  }
  
  .form-group label {
    display: block;
    font-size: 1rem;
    margin-bottom: 0.5rem;
  }
  
  .form-group input {
    width: 100%;
    padding: 0.8rem;
    font-size: 1rem;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  .form-group input:focus {
    border-color: #007BFF;
  }
  
  .form-actions {
    text-align: center;
    margin-top: 1.5rem;
  }
  
  .login-btn {
    padding: 0.8rem 2rem;
    font-size: 1rem;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    width: 100%;
  }
  
  .login-btn:hover {
    background-color: #0056b3;
  }
  
  .forgot-password {
    text-align: center;
    margin-top: 1rem;
    font-size: 0.9rem;
  }
  
  .forgot-password a {
    color: #007BFF;
    text-decoration: none;
  }
  
  .forgot-password a:hover {
    text-decoration: underline;
  }
</style>
  