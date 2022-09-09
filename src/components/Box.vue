<template>
  <div>
    <div class="box" @mouseover="handleEvents($event, 5)"></div>
    <div class="box" @mouseleave="handleEvents"></div>
    <div class="box" @dbclick="handleEvents"></div>
    <div class="box" @mousemove="handleMouseMove">position-{{ x }}-{{ y }}</div>
  </div>
</template>

<script>
export default {
  name: "box-com",
  data() {
    return {
      x: 0,
      y: 0,
    };
  },
  methods: {
    handleEvents(e, data) {
      console.log(e, e.type);
      if (data) {
        console.log(data);
      }
    },
    handleMouseMove(e) {
      this.x = e.offsetX;
      this.y = e.offsetY;
    },
  },
};
</script>

<style>
.box {
  padding: 100px 0px;
  width: 400px;
  text-align: center;
  background-color: #ddd;
  margin: 20px;
  display: inline-block;
}
</style>
