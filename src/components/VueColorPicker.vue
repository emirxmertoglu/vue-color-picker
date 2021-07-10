<template>
  <div class="main">
    <a
      href="#"
      class="color"
      :style="{ backgroundColor: color }"
      @click="status = !status"
    ></a>
    <div class="color-palette" v-show="status">
      <ul>
        <li class="row">
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#1EBC9B' }"
            @click="color = '#1EBC9B'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#1BA085' }"
            @click="color = '#1BA085'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#2DCC70' }"
            @click="color = '#2DCC70'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#26AF5F' }"
            @click="color = '#26AF5F'"
          ></a>
        </li>
        <li class="row">
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#3297DB' }"
            @click="color = '#3297DB'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#297FB8' }"
            @click="color = '#297FB8'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#A463BF' }"
            @click="color = '#A463BF'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#8F44AD' }"
            @click="color = '#8F44AD'"
          ></a>
        </li>
        <li class="row">
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#3D556F' }"
            @click="color = '#3D556F'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#22303D' }"
            @click="color = '#22303D'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#F2C510' }"
            @click="color = '#F2C510'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#F19D19' }"
            @click="color = '#F19D19'"
          ></a>
        </li>
        <li class="row">
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#E84B3C' }"
            @click="color = '#E84B3C'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#C0382C' }"
            @click="color = '#C0382C'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#DDE7E9' }"
            @click="color = '#DDE7E9'"
          ></a>
          <a
            href="#"
            class="color"
            :style="{ backgroundColor: '#BEC3C9' }"
            @click="color = '#BEC3C9'"
          ></a>
        </li>
      </ul>
      <div class="result">
        <input
          type="color"
          name="picker"
          id="picker"
          class="picker"
          :value="color"
          @change="setColor"
        />
        <a href="#" class="ok" @click="status = !status">Ok</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      color: "#424242",
      status: false,
    };
  },
  methods: {
    setColor(e) {
      this.color = e.target.value;
    },
  },
};
</script>

<style lang="scss" scoped>
* {
  padding: 0;
  margin: 0;
  list-style: none;
  border: none;
  text-decoration: none;
  box-sizing: border-box;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  &:focus {
    outline: 0;
  }
}

.main {
  .color {
    display: block;
    margin: 5px 5px;
    width: 40px;
    height: 40px;
    border-radius: 10px;
    background-color: #424242;
  }

  .color-palette {
    display: inline-block;
    margin: 10px 10px;
    background: #fff;
    border: 1px solid #ccc;
    border-radius: 10px;
    box-shadow: rgba(0, 0, 0, 0.35) 0px 2px 7px;

    .row {
      display: flex;
      margin: 10px 10px;
    }

    .result {
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 15px 15px;

      .picker {
        flex: 1;
        display: flex;
        height: 25px;
        margin-right: 10px;
      }
      .ok {
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 14px;
        font-weight: 500;
        background: #1976d2;
        color: #fff;
        width: 50px;
        height: 25px;
        border-radius: 10px;
      }
    }
  }
}
</style>