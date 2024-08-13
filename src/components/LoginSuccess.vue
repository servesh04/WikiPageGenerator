<template>
    <div class="login-success">
      <h1>Login Successful!</h1>
      <p>Welcome, {{ username }}!</p>
      <!-- Display protected content or navigate to a protected area -->
    </div>
  </template>
  
  <script>
  export default {
    name: 'LoginSuccess',
    computed: {
      username() {
        // Retrieve the username from the authentication data
        const token = new URLSearchParams(window.location.search).get('token');
        // Decode the token or perform any necessary operations to get the username
        return 'User';
      }
    }
  }
  </script>