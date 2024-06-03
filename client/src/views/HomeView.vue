<template>
  <main>
    <br>
    <br>
    <h1>TMP</h1>
    <p>Please sign in or create an account to continue.</p>
    <br>
    <br>
    <div class="buttons">
      <router-link to="/login" class="button">Login</router-link>
      <router-link to="/register" class="button">Sign Up</router-link>
    </div>
  </main>
</template>

<script setup lang="ts">
</script>

<style scoped>
/* Styles for the home page */
main {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
}
body{
  background-color: red;
}
h1 {
  font-size: 2.5rem;
  margin-bottom: 30px;
}

p {
  font-size: 1.2rem;
  margin-bottom: 20px;
}

.buttons {
  display: flex;
  justify-content: center;
}

.button {
  margin: 0 10px;
  padding: 10px 20px;
  text-decoration: none;
  background-color: #007bff;
  color: #fff;
  border: 1px solid #007bff;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: #0056b3;
}

.button:active {
  background-color: #0056b3;
}
</style>
