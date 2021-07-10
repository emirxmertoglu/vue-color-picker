<template>
  <div id="app">
    Click and choose a color
    <VueColorPicker />
  </div>
</template>

<script>
import VueColorPicker from "./components/VueColorPicker.vue";

export default {
  name: "App",
  components: { VueColorPicker },
};
</script>