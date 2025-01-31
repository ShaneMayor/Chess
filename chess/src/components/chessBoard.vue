<template>
  <div class="mainBoard">
    <div v-for="row in 8" :key="row" class="row">
      <div v-for="col in 8" :key="col" :class="['cell', (row + col) % 2 === 0 ? 'white' : 'black']"></div>
    </div>
  </div>
</template>

<style scoped>
.mainBoard {
  display: grid;
  grid-template-rows: repeat(8, 1fr);
  grid-template-columns: repeat(8, 1fr);
  width: 600px;
  height: 600px;
  border: 5px solid burlywood;
  box-shadow: 0 0 0 20px green; 
}

.row {
  display: contents;
}

.white {
  background-color: white;
}

.black {
  background-color: black;
}
</style>