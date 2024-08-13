<template>
    <div class="screen">
    <form>
      <H1>WIKI PAGE GENERATOR</H1>
    <input type="text" placeholder="Email" name="email" required>
    <input type="password" placeholder="Password" name="password" required>
    <input type="submit" value="Login">
    <button class="google-btn" @click="authenticateWithGoogle">SignIn with Google</button>
  </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'LoginPage',
    methods: {
      authenticateWithGoogle() {
        window.location.href = 'http://localhost:5000/auth/google';
      }
    }
  }
  </script>
  
  <style scoped>
  
  .screen {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #4f46e5;
  color: #ffffff;
  
}

form {
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  background: linear-gradient(to bottom, #334155, #1e293b);
  border-radius: 1rem;
  box-shadow: 0 0 1rem rgba(0, 0, 0, 0.2);
}

form::before {
  content: '';
  position: absolute;
  left: -25%;
  top: -25%;
  height: 150%;
  width: 150%;
  /* background: conic-gradient(rgba(244, 114, 182, 0.4) 0deg, rgba(192, 132, 252, 0.4) 0deg, transparent 80deg); */
  /* animation: border-spin 3s infinite linear; */
}

h1 {
  font-size: 2rem;
  margin-bottom: 1.5rem;
  z-index: 1;
}

input[type="text"],
input[type="password"] {
  width: 100%;
  padding: 0.75rem;
  margin-bottom: 1rem;
  border: none;
  border-radius: 0.25rem;
  background-color: #334155;
  color: #ffffff;
  z-index: 1;
}

input[type="text"]::placeholder,
input[type="password"]::placeholder {
  color: #94a3b8;
}

input[type="submit"],
.google-btn {
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 0.25rem;
  background-color: #4f46e5;
  color: #ffffff;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s ease;
  z-index: 1;
}

input[type="submit"]:hover,
.google-btn:hover {
  background-color: #6366f1;
}

.google-btn {
  margin-top: 1rem;
  background-color: #03ff1c;
  color: #0f172a;
}

.google-btn:hover {
  background-color: #04b42a;
}

  </style>