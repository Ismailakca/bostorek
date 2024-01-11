<template lang="">
  <nav class="navbar navbar-expand-md custom-nav">
    <div class="container">
      <a href="#" class="navbar-brand">Bots</a>
      <ul class="navbar-nav">
        <li class="nav-item">
          <a href="#" class="nav-link">Books</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Contact Us</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Login</a>
        </li>
        <li class="nav-item">
          <a href="#" class="nav-link">Register</a>
        </li>
      </ul>
    </div>
  </nav>
</template>
<script>
export default {
  name: "NavBar",
};
</script>
<style scoped>
.custom-nav {
  background-color: #063547;
  padding: 15px 0;
}

.navbar-brand {
  padding: 0;
  margin: 0;
  color: #fff;
  fontweight: bold;
  font-size: 24px;
}

.nav-link {
  padding: 10px 25px;
  color: #fff;
  text-align: center;
}
</style>
