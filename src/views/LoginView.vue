<template>
    <div class="login-container">
      <!-- Using the LoginComponent as part of the view -->
      <login-comp/>
    </div>
  </template>
  
  <script>
  import LoginComp from '../components/LoginComp.vue'; // Import login component
  
  export default {
    name: 'LoginView',
    components: {
      LoginComp
    }
  }
  </script>
  
  <style scoped>
  .login-container {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f7f7f7;
  }
  </style>
  