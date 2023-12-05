<template>
    <footer>
      <div class="footer-container">
        <div class="footer-section">
          <h3>Doc Check</h3>
        </div>

      </div>
  
      <div class="copyright">
        <p>&copy; 2023 All rights reserved.</p>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
  };
  </script>
  
  <style scoped>
  footer {
    background-color: #333;
    color: white;
    padding: 20px 0;
    text-align: center;
  }
  
  .footer-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }
  
  .footer-section {
    margin-bottom: 20px;
  }
  
  h3 {
    margin-bottom: 10px;
  }
  
  .social-icons {
    display: flex;
  }
  
  .icon-link {
    margin-right: 10px;
    color: white;
    text-decoration: none;
  }
  
  .copyright {
    background-color: #222;
    padding: 10px 0;
  }
  </style>
  