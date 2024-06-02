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
  <footer>
      <h2>Pet project by <span>TFM</span></h2>
      <a :href="githubLink">GitHub</a>
  </footer>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'

const githubLink = "https://github.com/TFatM";
</script>


<style lang="scss">

@font-face {
    font-family: MPlusRounded;
    src: url('./assets/fonts/MPLUSRounded1c-Regular.ttf') format('truetype');
  }

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
    font-family: MPlusRounded;

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

    footer{
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      margin-bottom: 8px;
      gap: 8px;

      h2{
        color: var(--color-brand-winterWhite);
        font-size: 18px;
        letter-spacing: 0.8px
      }

      a{
        color: var(--color-brand-winterWhite);
        text-decoration: underline;
        transition: .3s;

        &:hover{
          color: var(--color-brand-black);
        }
      }
    }
  }
</style>
