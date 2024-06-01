<template>
  <header>
    <router-link
    to="/">
      <h1><span>TFM</span> Movies</h1>
    </router-link>
  </header>
  <main>
    <router-view />
  </main>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>


<style lang="scss">
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family:Arial, Helvetica, sans-serif;

    &::selection{
      background: transparentize(#42B883, 0.5);
    }

    body{
      background-color: #2b364b;
    }

    a{
      text-decoration: none;
    }

    header{
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 10px 16px;
      background-color: #2C3D4E;
      box-shadow: 0px 0px 6px rgba(0, 0, 0, 0.2);
    }

    h1{
      color: #fff;
      font-size: 28px;
      letter-spacing: 0.8px
    }

    span{
      color: #42B883;
    }
  }
</style>
