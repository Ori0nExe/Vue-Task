// TheFloor.vue
<template>
  <div class="floor">
    <button 
      :class="[floorNumber === currentFloor ? 'green' : callMade ? 'active' : 'button']" 
      @click="callElevator">
      {{ floorNumber === currentFloor ? 'Текущий этаж' : 'Вызвать на этаж номер ' + floorNumber }}
    </button>
  </div>
</template>



<script>
export default {
  props: ['floorNumber', 'currentFloor'],
  data() {
    return {
      callMade: false
    }
  },
  methods: {
    callElevator() {
      this.callMade = true;
      this.$emit('callElevator', this.floorNumber);

      setTimeout(() => {
        this.callMade = false;
      }, 5000); 
    }
  }
};
</script>

<style scoped>
.floor {
  border:  1px dotted black;
  padding: 50px;
  display: flex;
  justify-content: end;
  background-color: gray;

}

.button {
  width: 175px;
  padding: 10px;
  background-color: #ccc;
  color: #333;
  border: none;
  border-radius: 5px;
}

.active {
  width: 175px;
  padding: 10px;
  background-color: red;
  color: #333;
  border: none;
  border-radius: 5px;
}

.green {
  width: 175px;
  padding: 10px;
  background-color: black;
  color: white;
  border: none;
  border-radius: 5px;
  }
</style>
