<template>
    <div>
      <Header />
      <div class = "page content"> 
      <div class="signup-container">
        <form class="signup-form">
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" name="email" placeholder="Email">
          </div>
          <div class="form-group">
            <label for="password">Password</label>
            <input type="password" id="password" name="password" placeholder="Password">
          </div>
          <button type="submit" class="signup-button">Signup</button>
        </form>
      </div>
    </div>
      <Footer />
    </div>
  </template>
  
  <script>
  import Header from '@/components/CompoHeader.vue';
  import Footer from '@/components/CompoFooter.vue';
  
  export default {
    components: {
      Header,
      Footer
    }
  };
  </script>
  
  <style scoped>
  .page-content {
    padding-top: 60px;
  }
  .signup-container {
    background-color: rgb(243, 255, 221); 
    padding: 20px;
    text-align: center;
    border-radius: 10px;
  }
  
  .signup-form {
    display: inline-block;
    margin-top: 20px;
  }
  
  .form-group {
    margin-bottom: 15px;
  }
  
  .form-group label {
    display: block;
    margin-bottom: 5px;
    color: black;
  }
  
  .form-group input {
    width: 100%;
    padding: 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
    background-color: white;
    color: lightgray;
  }
  
  .signup-button {
    background-color: rgb(122, 175, 255);
    color: black;
    padding: 10px 15px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .signup-button:hover {
    background-color: rgb(122, 175, 255); 
  }
  </style>
  