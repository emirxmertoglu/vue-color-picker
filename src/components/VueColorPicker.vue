<template>
  <div class="main">
    <div class="head">
      <h3 class="title">Choose a color:</h3>
      <input type="color" name="color" id="color" @change="setColor" />
    </div>
    <h3 :style="{ color: color }">Hex code: {{ color }}</h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      color: "",
    };
  },
  methods: {
    setColor(e) {
      this.color = e.target.value;
    },
  },
};
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
}

.head {
  display: flex;
  align-items: center;
}

.head .title {
  margin-right: 8px;
}
</style>