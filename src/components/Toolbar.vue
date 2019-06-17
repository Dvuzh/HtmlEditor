<template>
  <div class="toolbar">
    <draggable v-model="myArray" group="people" @start="drag=true" @end="drag=false">
      <div v-for="element in myArray" :key="element.id">{{element.name}}</div>
    </draggable>
  </div>
</template>

<script>
import draggable from "vuedraggable";

export default {
  name: "Toolbar",
  components: { draggable },
  data: function() {
    return {
      myArray: [
        {
          id: 1,
          name: "Katya"
        },
        {
          id: 2,
          name: "Vasya"
        }
      ]
    };
  }
};
</script>

<style>
.toolbar {
  width: 30%;
  height: 500px;
  border: 1px solid red;
  align-self: center;
}
</style>