<template>
  <div class="home">

    <carousel v-bind="settings" :breakpoints="breakpoints" :wrapAround="true">
      <slide v-for="slide in 1" :key="slide">
        <div class="feature-card carousel__item">
        <router-link to="/movie/tt0388629">
        <img src="https://m.media-amazon.com/images/M/MV5BM2YwYTkwNjItNGQzNy00MWE1LWE1M2ItOTMzOGI1OWQyYjA0XkEyXkFqcGdeQXVyMTUzMTg2ODkz._V1_SX300.jpg" 
        alt="One piece Poster" 
        class="featured-img">
        <div class="detail">
          <h3>One piece</h3>
          <p>Monkey D. Luffy sets off on an adventure with his pirate crew in hopes of finding the greatest treasure
            ever, known as the One Piece.</p>
          </div>
        </router-link>
      </div>
      </slide>
      <slide v-for="slide in 1" :key="slide">
        <div class="feature-card carousel__item">
          <router-link to="/movie/tt0831387">
            <img src="https://m.media-amazon.com/images/M/MV5BZDFmYTM4NzAtNWM0ZC00MGJlLWEyYzQtYzA3ZTFiNzc1YjllXkEyXkFqcGdeQXVyMTA4NjE0NjEy._V1_SX300.jpg" 
            alt="Godzilla Poster" 
            class="featured-img">
            <div class="detail">
              <h3>Godzilla</h3>
              <p>The world is beset by the appearance of monstrous creatures, but one of them may be the only one who can save humanity.</p>
            </div>
          </router-link>
        </div>
      </slide>
      <slide v-for="slide in 1" :key="slide">
        <div class="feature-card carousel__item">
          <router-link to="/movie/tt6644200">
            <img src="https://m.media-amazon.com/images/M/MV5BMjI0MDMzNTQ0M15BMl5BanBnXkFtZTgwMTM5NzM3NDM@._V1_SX300.jpg" 
            alt="A Quiet Place Poster" 
            class="featured-img">
            <div class="detail">
              <h3>A Quiet Place</h3>
              <p>A family struggles for survival in a world where most humans have been killed by blind but noise-sensitive creatures. They are forced to communicate in sign language to keep the creatures at bay.</p>
            </div>
          </router-link>
        </div>
      </slide>
      <slide v-for="slide in 1" :key="slide">
        <div class="feature-card carousel__item">
          <router-link to="/movie/tt22248376">
            <img src="https://m.media-amazon.com/images/M/MV5BMjVjZGU5ZTktYTZiNC00N2Q1LThiZjMtMDVmZDljN2I3ZWIwXkEyXkFqcGdeQXVyMTUzMTg2ODkz._V1_SX300.jpg" 
        alt="Frieren: Beyond Journey's End Poster" 
        class="featured-img">
        <div class="detail">
          <h3>Frieren: Beyond Journey's End</h3>
          <p>An elf and her friends defeat a demon king in a great war. But the war is over, and the elf must search for a new way of life.</p>
        </div>
      </router-link>
    </div>
  </slide>
  <slide v-for="slide in 1" :key="slide">
    <div class="feature-card carousel__item">
      <router-link to="/movie/tt1865718">
              <img src="https://m.media-amazon.com/images/M/MV5BMTEzNDc3MDQ2NzNeQTJeQWpwZ15BbWU4MDYzMzUwMDIx._V1_SX300.jpg" 
              alt="Gravity Falls Poster" 
              class="featured-img">
              <div class="detail">
                <h3>Gravity Falls</h3>
                <p>Twin siblings Dipper and Mabel Pines spend the summer at their great-uncle's tourist trap in the enigmatic Gravity Falls, Oregon.</p>
              </div>
            </router-link>
          </div>
        </slide>
        <slide v-for="slide in 1" :key="slide">
          <div class="feature-card carousel__item">
            <router-link to="/movie/tt1877830">
              <img src="https://m.media-amazon.com/images/M/MV5BM2MyNTAwZGEtNTAxNC00ODVjLTgzZjUtYmU0YjAzNmQyZDEwXkEyXkFqcGdeQXVyNDc2NTg3NzA@._V1_SX300.jpg" 
        alt="The Batman Poster" 
        class="featured-img">
        <div class="detail">
          <h3>The Batman</h3>
          <p>When a sadistic serial killer begins murdering key political figures in Gotham, Batman is forced to investigate the city's hidden corruption and question his family's involvement.</p>
        </div>
      </router-link>
    </div>
  </slide>
  <slide v-for="slide in 1" :key="slide">
    <div class="feature-card carousel__item">
      <router-link to="/movie/tt0084787">
              <img src="https://m.media-amazon.com/images/M/MV5BNGViZWZmM2EtNGYzZi00ZDAyLTk3ODMtNzIyZTBjN2Y1NmM1XkEyXkFqcGdeQXVyNTAyODkwOQ@@._V1_SX300.jpg" 
        alt="The Thing Poster" 
        class="featured-img">
        <div class="detail">
          <h3>The Thing</h3>
          <p>A research team in Antarctica is hunted by a shape-shifting alien that assumes the appearance of its victims.</p>
        </div>
      </router-link>
    </div>
  </slide>
    <slide v-for="slide in 1" :key="slide">
    <div class="feature-card carousel__item">
            <router-link to="/movie/tt4154796">
        <img src="https://m.media-amazon.com/images/M/MV5BMTc5MDE2ODcwNV5BMl5BanBnXkFtZTgwMzI2NzQ2NzM@._V1_SX300.jpg" 
        alt="Avengers: Endgame Poster" 
        class="featured-img">
        <div class="detail">
          <h3>Avengers: Endgame</h3>
          <p>After the devastating events of Avengers: Infinity War (2018), the universe is in ruins. With the help of remaining allies, the Avengers assemble once more in order to reverse Thanos' actions and restore balance to the universe.</p>
        </div>
      </router-link>
    </div>
      </slide>

      <template #addons>
      <Navigation />
    </template>
    </carousel>

    <form 
    @submit.prevent="SearchMovies()" 
    class="search-box">
      <input 
      type="text"
      placeholder="What are you searching?"
      v-model="search">
      <input 
      type="submit" 
      value="Search">
    </form>

    <div class="movies-list">
      <div class="movie"
      v-for="movie in movies"
      :key="movie.imdbID">
        <router-link
        :to="'/movie/' + movie.imdbID"
        class="movie-link">
        <div class="product-image">
        <img :src="movie.Poster" 
        alt="Movie Poster">
        <div class="type">{{ movie.Type }}</div>
        </div>
        <div class="detail">
          <p class="year">{{ movie.Year }}</p>
          <h3>{{ movie.Title }}</h3>
        </div>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import { ref, defineComponent } from 'vue';
import env from '@/env.js';

import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Navigation } from 'vue3-carousel';

export default defineComponent({
  name: 'Home',
  components: {
    Carousel,
    Slide,
    Navigation,
  },
  setup() {
    const search = ref("");
    const movies = ref([]);

    const SearchMovies = () => {
      if (search.value !== "") {
        fetch(`http://www.omdbapi.com/?apikey=${env.apikey}&s=${search.value}`)
          .then(response => response.json())
          .then(data => {
            movies.value = data.Search;
            search.value = "";
          });
      }
    };

    // carousel settings
    const settings = ref({
      itemsToShow: 1,
      snapAlign: 'center',
    });

    // breakpoints settings
    const breakpoints = ref({
      700: {
        itemsToShow: 3.5,
        snapAlign: 'center',
      },
      1024: {
        itemsToShow: 6,
        snapAlign: 'start',
      },
    });

    return {
      search,
      movies,
      SearchMovies,
      settings,
      breakpoints,
    };
  },
});
</script>

  <style lang="scss">



  .home {

    .carousel{
      overflow: hidden;

      .carousel__prev,
      .carousel__next{
        height: 50px;
        width: 50px;
        margin: 0;
        background-color: var(--color-brand-lightBlue);
        border-radius: 0px 50% 50% 0px;
      }
    }

    .feature-card {
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      max-width: 300px;

      .featured-img {
        display: block;
        width: 100%;
        height: 300px;
        object-fit: fill;
        position: relative;
        z-index: 0;
        
      }

      .detail {
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(0, 0, 0, 0.5);
        padding: 16px;
        z-index: 1;
        

        h3 {
          text-transform: uppercase;
          color: var(--color-brand-white);
          margin-bottom: 16px;
        }

        p {
          color: var(--color-brand-white);
        }
      }
    }

    .search-box{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 16px;

      input{
        display: block;
        appearance: none;
        border: none;
        outline: none;
        background: none;

        &[type="text"] {
          width: 100%;
          color: var(--color-brand-white);
          background-color: var(--color-brand-lightBlue);
          font-size: 20px;
          padding: 10px 16px;
          border-radius: 8px;
          margin-bottom: 15px;
          transition: .4s;
          
          &::placeholder{
            color: #f3f3f3;
          }
          
          &:focus{
            box-shadow: 0px 3px 0px rgba(0, 0, 0, 0.2);
          }
        }

        &[type="submit"]{
          width: 100%;
          max-width: 300px;
          background-color: var(--color-brand-green);
          padding: 16px;
          border-radius: 8px;
          color: #fff;
          font-size: 20px;
          text-transform: uppercase;
          transition: .4s;

          &:active{
            background-color: var(--color-secondary-green);
          }
        }
      }
    }

    .movies-list{
      display: flex;
      flex-wrap: wrap;
      margin: 0px 8px;
      
      .movie{
        max-width: 50%;
        flex: 1 1 50%;
        padding: 16px 8px;
        @media screen and (min-width: 768px)  {
          display: flex;
          margin-right: auto;
          margin-left: auto;
          flex: none;
        }
      
        .movie-link{
        display: flex;
        flex-direction: column;
        height: 100%;

        .product-image{
        position: relative;
        display: block;

          img{
            display: block;
            width: 100%;
            max-height: 275px;
            object-fit: cover;

            @media screen and (min-width: 768px)  {
          max-height: 450px;
          width: auto;
          object-fit: contain;
        }
          }

          .type{
          position: absolute;
          padding: 8px 16px;
          background-color: var(--color-brand-green);
          color: var(--color-brand-white);
          bottom: 16px;
          left: 0;
          text-transform: capitalize;
          }

        }
        .detail{
          background-color: var(--color-brand-lightBlue);
          padding: 16px 8px;
          flex: 1 1 100%;
          border-radius: 0px 0px 8px 8px;
          
          .year{
            color: #AAA;
            font-size: 14px;
            margin-bottom: 5px;
          }
  
          h3{
            color: var(--color-brand-white);
            font-weight: 600;
            font-size: 18px;
            transition: color .3s;
          }
        }
      }
    }
  }
}
</style>