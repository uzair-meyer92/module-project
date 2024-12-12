<template>
    <header>
      <h1>HR Dashboard</h1>
      <nav>
        <ul>
          <li><a href="#leave-requests" @click="scrollToSection('leave-requests')">Leave Requests</a></li>
          <li><a href="#payroll" @click="scrollToSection('payroll')">Payroll & Payslips</a></li>
          <li><a href="#performance-metrics" @click="scrollToSection('performance-metrics')">Performance Metrics</a></li>
          <li><a href="#employee-info" @click="scrollToSection('employee-info')">Employee Info</a></li>
        </ul>
      </nav>
    </header>
</template>
  
<script>
  export default {
    methods: {
      scrollToSection(sectionId) {
        const element = document.getElementById(sectionId);
        if (element) {
          window.scrollTo({
            top: element.offsetTop - 50, // Adjust for any fixed navbar
            behavior: 'smooth'
          });
        }
      }
    }
  };
</script>
  
<style scoped>
  header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
  }
  
  nav ul {
    list-style-type: none;
    padding: 0;
  }
  
  nav ul li {
    display: inline;
    margin-right: 20px;
  }
  
  nav ul li a {
    color: white;
    text-decoration: none;
    font-size: 18px;
    font-weight: bold;
  }
  
  nav ul li a:hover {
    color: #ff6347;
  }
</style>
  