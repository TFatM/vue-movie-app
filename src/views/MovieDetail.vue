<template>
  <div class="movie-detail">
    <div class="movie-mainInfo">
      <h2>{{ movie.Title }}</h2>
      <div class="movie-mainInfo__container">
        <p>{{ movie.Year }}</p>
        <p>{{ movie.Genre }}</p>
        <p>Rated:{{ movie.Rated }}</p>
      </div>
    </div>
    <img 
    :src="movie.Poster" 
    alt="Movie Poster"
    class="featured-img">
    <div class="movie-ratings">
      <h2>Ratings:</h2>
      <div class="movie-ratings__wrap">
        <div class="movie-ratings__imdb">
          <img :src="imdbLogo">
          <p>IMDB Rating: {{ movie.imdbRating }}</p>
        </div>
        <div class="movie-ratings__metascore">
          <img :src="metascoreLogo">
          <p>Metascore Rating: {{ movie.Metascore }}</p>
        </div>
      </div>
    </div>
    <div class="movie-infoWrap">
      <div class="movie-plot">
        <h2>Plot:</h2>
        <p>{{ movie.Plot }}</p>
      </div>
      <div class="movie-secondInfo">
        <h2>Info:</h2>
        <p><b>Director:</b> {{ movie.Director }}</p>
        <p><b>Actors:</b> {{ movie.Actors }}</p>
        <p><b>Country:</b> {{ movie.Country }}</p>
        <p><b>Runtime:</b> {{ movie.Runtime }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, onBeforeMount } from 'vue';
import { useRoute } from 'vue-router';
import env from '@/env.js';
import imdbLogo from '../img/imdb.svg'
import metascoreLogo from '../img/metascore.svg'

export default {
  setup() {
    const movie = ref({});
    const route = useRoute();

    onBeforeMount(() => {
      fetch(`https://www.omdbapi.com/?apikey=${env.apikey}&i=${route.params.id}&plot=full`)
        .then(response => response.json())
        .then(data => {
          movie.value = data;
          console.log(data);
        });
    });
    
    return{
      movie,
      imdbLogo,
      metascoreLogo
    }
  }
}
</script>

<style lang="scss">
.movie-detail{
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 16px;

  .movie-mainInfo{
    display: flex;
    flex-direction: column;
    background-color: var(--color-brand-lightBlue);
    width: 100%;
    margin-bottom: 16px;
    padding: 8px;
    border-radius: 8px;

    &__container{
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
    }
  }

  
  h2{
    color: var(--color-brand-white);
    font-size: 28px;
    font-weight: 600px;
    margin-bottom: 16px;
  }
  
  .featured-img{
    display: block;
    max-width: 100%;
    margin-bottom: 16px;
  }
  
  p{
    color: var(--color-brand-white);
    font-size: 18px;
    line-height: 1.4;
  }

  .movie-ratings{
    display: flex;
    flex-direction: column;
    width: 100%;
    background-color: var(--color-brand-lightBlue);
    border-radius: 8px;
    padding: 8px;

    &__wrap{
      display: flex;
      justify-content: space-evenly;
      gap: 12px;
    }

    &__imdb{
      display: flex;
      justify-items: center;
      align-items: center;
      gap: 8px;

      img{
        width: 24px;
        height: 24px;
      }
    }

    &__metascore{
      display: flex;
      justify-items: center;
      align-items: center;
      gap: 8px;

      img{
        width: 24px;
        height: 24px;
      }
    }
  }

  .movie-infoWrap{
    display: block;

    @media screen and (min-width: 768px)  {
      display: flex;
      gap: 20px;
      margin-top: 15px;
    }
  }

  .movie-plot{
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    width: 100%;
    margin: 16px auto;
    background-color: var(--color-brand-lightBlue);
    border-radius: 8px;
    padding: 8px;
  }

  .movie-secondInfo{
    display: flex;
    flex-direction: column;
    gap: 18px;
    background-color: var(--color-brand-lightBlue);
    border-radius: 8px;
    padding: 8px;

    p{
      border-bottom: 3px solid var(--color-brand-winterWhite);
    }
  }
}
</style>