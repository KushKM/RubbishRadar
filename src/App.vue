<script setup>
  import { ref } from "vue";
  import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <nav>
      <RouterLink class="homeLink" to = "/"> Home </RouterLink>
      <RouterLink class="aboutLink" to = "/about"> About </RouterLink>
      <RouterLink class="userAuthLink" to = "/UserAuth"> Login / SignUp </RouterLink>
    </nav>  
  <RouterView/>
</template>

<style scoped>

nav {
  display: flex;
  position: absolute;
  font-size: 1rem;
  right: 0;
  top: 0;
  background-color: #31c48d;
  width: 100%;
  justify-content: right;
  padding-top: 10px;
  padding-bottom: 10px;
  z-index: 9999;
}

nav a.router-link-exact-active {
  color: black;
  font-weight: bold;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
  background-color: #3be1a4;
  border-radius: 30px;
}

nav a {
  margin-right: 10px;
  color: black;
  display: block;
  padding: 0 2rem;
  border-left: 1px solid var(--color-border);
  transition: 0.5s;
  text-decoration: none;
}

nav a:hover {
  /* font-weight: bold; */
  background-color: #3be1a4;
  border-radius: 30px;
  /* padding: 10px; */
}

nav a:first-of-type {
  border: 0;
}

/* nav a::after {
  position: absolute;
  content: '';
  width: 100%;
  height: 3px;
  top: 100%;
  left: 0;
  transition: transform 0.5s;
  transform: scaleX(0);
  transform-origin: right;
  background-color: black;
}

nav a:hover::after {
  transform: scaleX(1);
  transform-origin: left;
} */

/* .homeLink::after {
  position: absolute;
  content: '';
  width: 5%;
  height: 1.5px;
  top: 70%;
  left: 75.5%;
  transition: transform 0.5s;
  transform: scaleX(0);
  transform-origin: right;
  background-color: black;
}

.homeLink:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}

.aboutLink::after {
  position: absolute;
  content: '';
  width: 3.3%;
  height: 1.5px;
  top: 70%;
  left: 83.6%;
  transition: transform 0.5s;
  transform: scaleX(0);
  transform-origin: right;
  background-color: black;
}

.aboutLink:hover::after {
  transform: scaleX(1);
  transform-origin: left;
}

.userAuthLink::after {
  position: absolute;
  content: '';
  width: 8%;
  height: 1.5px;
  top: 80%;
  left: 90%;
  transition: transform 0.5s;
  transform: scaleX(0);
  transform-origin: right;
  background-color: black;
}

.userAuthLink:hover::after {
  transform: scaleX(1);
  transform-origin: left;
} */

@media (min-width: 1024px) {
  nav {
    font-size: 1rem;
  }
}
</style>
