<script setup>
  import { ref } from 'vue';

  const columns = ref(15);
  const rows = ref(6);

</script>

<template>
  <div class="about">
    <h1>Happy Birthday!</h1>
    <div class="wrapper">
      <img src="../assets/guitar-bg.png" alt="guitar-background">
      <div class="game">
        <!-- 15 x 6 -->
        <div class="column" v-for="column in columns">
          <div class="row" v-for="row in rows">
            <div class="cell">
              {{ column }}
            </div>
          </div>
        </div>
          


        
      </div>
    </div>
  </div>
</template>

<style scoped>



@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  img {
    z-index: 1;
  }

  .wrapper {
    background-color: white;
    /* min-height: 100vh; */
    /* display: flex; */
    /* align-items: center; */
  }

  .game {
    width: 887px;
    height: 156px;
    display: grid;
    grid-template-columns: repeat(15, 1fr);
    grid-template-rows: repeat(6, 1fr);
    z-index: 5;
    position: relative;
    top: -198px;
    left: 10px;
    border: 2px solid red;
  }

  .column .row {
    
  }

  .cell {
    background-color: #214f3343;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
