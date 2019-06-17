<template>
  <div class="left-block">
    <Toolbar />
  </div>
</template>

<script>
import Toolbar from "./Toolbar";

export default {
  name: "LeftMenu",
  components: {
    Toolbar
  }
};
</script>

<style>
.left-block {
  width: 30%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-content: center
  /* align-self: center; */
  /* align-items: center; */
}
</style>