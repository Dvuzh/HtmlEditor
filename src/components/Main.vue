
    <template>
  <table>
    <draggable v-model="list" :element="'thead'">
      <tr>
        <th>Colors</th>
        <th v-for="(color, i) in list" :key="i">{{color}}</th>
      </tr>
    </draggable>
    <tbody>
      <tr>
        <td>Number</td>
        <td v-for="(color, i) in list" :key="i">{{data[color]}}</td>
      </tr>
    </tbody>
  </table>
</template>



<script>
import draggable from "vuedraggable";

export default {
  name: "Main",
  components: { draggable },
  data() {
    return {
      list: ["red", "yellow", "blue"],
      data: { red: 1, yellow: 2, blue: 3 }
    };
  }
};
//
</script>

<style>
.center-block {
  width: 70%;
}
</style>