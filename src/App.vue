<template>
  <!-- <TheFloor></TheFloor> -->
  <ElevatorShaft></ElevatorShaft>
  <!-- <TheElevator></TheElevator> -->
</template>

<script>
import ElevatorShaft from './components/ElevatorShaft.vue';

export default {
  name: 'App',
  components: {
    ElevatorShaft
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
