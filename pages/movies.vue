<template>
    <div class="container">
  
      <div class="divButton">
        <NuxtLink to="/">
          <p class="backButton"> Atrás </p>
        </NuxtLink>
      </div>
  
      <h2 class="title"> Películas </h2>
  
      <Form v-for="movie in movies" :key="movie.name" :movie="movie" :available="movie.available" />
  
    </div>
</template>
  
<script>
    export default {
        data() {
        return {
            movies: [
            {
                name: "Revengers",
                maxTickets: 12,
            },
            {
                name: "SpuderMoon",
                maxTickets: 10,
            },
            {
                name: "BaturuMan",
                maxTickets: 8,
            },
            {
                name: "JourneyRabbit",
                maxTickets: 2,
            },
            ],
        };
        },
    };
</script>
  
<style scoped>
    .container {
        transform: translateY(-3.9vh);
        display: grid;
        justify-self: center;
        height: 100vh;
        width: 90vw;
        text-align: center;
    }
    
    .title {
        color: white;
        text-align: center;
        text-shadow: 3px 3px 6px black;
    }
    
    .divButton {
        transform: translate(-30vw, 9.9vh);
        display: absolute;
        justify-content: start;
    }
    
    .backButton {
        text-align: center;
        color: white;
        background-color: #4781FF;
        width: 15vh;
        border-radius: 12px;
        padding: 3px 0 3px;
    }
    
    .backButton {
        color: white;
        text-decoration: none;
        font-size: 15px;
    }
    
    .backButton:hover {
        color: yellow;
        transform: scale(1.2);
    }
</style>
  