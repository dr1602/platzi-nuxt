<template>
    <div class="main">
      <h3 class="title">¡FELICIDADES!</h3>
      <p class="paragraph">Has comprado {{ $route.query.count }} boleto(s) de la película {{ $route.query.name }}.</p>
  
      <div class="divButton">
        <nuxt-link to="/movies">
          <p class="devolverButton">Devolverlos</p>
        </nuxt-link>
      </div>
    </div>
</template>
  
<script>
    export default {
        name: 'PayPage',
    };
</script>
  
<style scoped>
    .main {
        display: grid;
        justify-self: center;
        height: 100vh;
        width: 90vw;
        text-align: center;
        background-image: url('https://i.pinimg.com/originals/02/64/e3/0264e3c2dce8496c2ba6dd37cb7a45b1.jpg');
        background-repeat: no-repeat;
        background-size: 72vw 100vh;
        background-position-x: center;
    }
    
    .title {
        color: white;
        text-align: center;
        text-shadow: 3px 3px 6px black;
        font-size: 30px;
    }
    
    .paragraph {
        color: white;
        text-align: center;
        text-shadow: 3px 3px 6px black;
        font-size: 30px;
    }
    
    .divButton {
        transform: translateY(0.9vh);
        display: flex;
        justify-content: center;
    }
    
    .devolverButton {
        color: white;
        text-align: center;
        background-color: #4781FF;
        width: 30vh;
        border-radius: 12px;
        padding: 6px 0 6px;
    }
    
    .devolverButton:hover {
        color: yellow;
        transform: scale(1.2);
    }
</style>
  