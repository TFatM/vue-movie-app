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
   :root{
  --color-brand-black: #1B262C;
  --color-brand-darkBlue: #0F4C75;
  --color-brand-lightBlue: #3282B8;
  --color-brand-winterWhite: #BBE1FA;
  --color-brand-green: #42B883;
  --color-secondary-green: #3B8070;
  --color-brand-white: #fff;
 }

  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family:Arial, Helvetica, sans-serif;

    &::selection{
      background: transparentize(#42B883, 0.5);
    }

    body{
      background-color: var(--color-brand-darkBlue);
    }

    a{
      text-decoration: none;
    }

    header{
      position: sticky;
      top: 0;
      z-index: 10;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 10px 16px;
      background-color: var(--color-brand-darkBlue);
      box-shadow: 0px 0px 6px rgba(0, 0, 0, 0.2);
    }

    h1{
      color: var(--color-brand-winterWhite);
      font-size: 28px;
      letter-spacing: 0.8px
    }

    span{
      color: var(--color-brand-green);
    }
  }
</style>
