<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import AddVideo from './views/AddVideo.vue';
</script>

<template>
    <header>
        <div>
            <nav>
                <RouterLink to="/">Home</RouterLink>
                <RouterLink to="/about">About</RouterLink>
            </nav>
        </div>
    </header>
    <div>
        <h1>hola</h1>
        <AddVideo />
    </div>
    <RouterView />
</template>

<style scoped>




nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}



@media (min-width: 1024px) {
  

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
