<template>
    <div class="forgot-password-form">
      <h1 class="forgot-password-title">Forgot Password</h1>
  
      <!-- Forgot Password Form -->
      <form @submit.prevent="handlePasswordReset">
        <div class="form-group">
          <label for="email">Enter your email</label>
          <input 
            type="email" 
            id="email" 
            v-model="email" 
            placeholder="Enter your email" 
            required
          />
        </div>
  
        <div class="form-actions">
          <button type="submit" class="reset-btn">Reset Password</button>
        </div>
      </form>
    </div>
</template>
  
<script>
  export default {
    name: 'ForgotPasswordComponent',
    data() {
      return {
        email: ''
      };
    },
    methods: {
      handlePasswordReset() {
        if (this.email) {
          // Reset link sent to email
          alert(`A password reset link has been sent to ${this.email}`);
        } else {
          // Display error message if email is not provided
          alert('Please enter your email'); 
        }
      }
    }
  }
</script>
  
<style scoped>
  .forgot-password-form {
    background-color: #fff;
    padding: 2rem;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 400px;
    margin: 0 auto;
    margin-top: 150px;
  }
  
  .forgot-password-title {
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
  
  .reset-btn {
    padding: 0.8rem 2rem;
    font-size: 1rem;
    background-color: #28a745;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    width: 100%;
  }
  
  .reset-btn:hover {
    background-color: #218838;
  }
</style>
  