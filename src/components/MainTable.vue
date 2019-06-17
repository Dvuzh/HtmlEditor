<template>
  <div class="toolbar">
    <!-- <draggable v-model="myArray" group="people" @start="drag=true" @end="drag=false">
      <div v-for="element in myArray" :key="element.id">{{element.name}}</div>
    </draggable>-->

    <table class="table">
      <thead>
        <tr>
          <td v-for="element in myArray" :key="element.id">{{element.name}}</td>
        </tr>
      </thead>
      <tbody>
          <th v-for="element in myArray" :key="element.id">
        <draggable v-model="element.items" @start="drag=true" @end="drag=false">
            <tr v-for="item in element.items" :key="item.id">{{item.name}}</tr>
        </draggable>
          </th>
      </tbody>
    </table>
  </div>
</template>

<script>
import draggable from "vuedraggable";

export default {
  name: "MainTable",
  components: { draggable },
  data: function() {
    return {
      myArray: [
        {
          id: 1,
          name: "To Do",
          items: [
            { id: 1, name: "Item 1", groupId: 1 },
            { id: 2, name: "Item 2", groupId: 1 },
            { id: 3, name: "Item 3", groupId: 1 }
          ]
        },
        {
          id: 2,
          name: "In Progress",
          items: [
            { id: 4, name: "Item 4", groupId: 2 },
            { id: 5, name: "Item 5", groupId: 2 },
            { id: 6, name: "Item 6", groupId: 2 }
          ]
        },
        {
          id: 3,
          name: "Done",
          items: [
            { id: 7, name: "Item 7", groupId: 3 },
            { id: 8, name: "Item 8", groupId: 3 },
            { id: 9, name: "Item 9", groupId: 3 },
            { id: 10, name: "Item 10", groupId: 3 }
          ]
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