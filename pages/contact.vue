<template>
    <div class="container">
        <ul class="menu">
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/contact">Contact</router-link></li>
        </ul>  
        <h1> 082126610058</h1>
        <ul class="contact">
            <li>Facebook</li>
            <li>whatshapp</li>
            <li>Instagram</li>

        </ul>
    </div>
  </template>
  
  </script>
  <style scoped>
  
    .container {
      width: 75%;
      margin: 100x auto;
      text-align: center;
    }
  
    .menu {
      list-style: none;
      margin-bottom: 20x;
    }
  
    
    .menu li {
      display: inline;
    }
  
    .menu li a {
      padding: 20px;
      text-decoration: none;
    }
     
  </style>