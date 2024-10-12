
<template>
  <div class="page-wrapper">
    <div class="canvas-wrapper"><canvas id="canvas"></canvas></div>
  </div>
</template>
 <!-- eslint-disable  -->
<script setup>

import *as fabric from 'fabric'

import { onMounted } from "vue";
let canvasElement;
let canvas;
function initCanvas() {
  canvasElement = document.getElementById("canvas");
  canvas = new fabric.Canvas(canvasElement, {
    height: 500,
    width: 100,
  });
}
onMounted(() => {
  initCanvas();
});
</script>
<style lang="scss" scoped>
.page-wrapper {
  .canvas-wrapper {
    width: 70%;
    height: auto; 
    display: flex;
    justify-content: center;
    align-items: center;
    -webkit-box-shadow: 1px -4px 15px -1px rgba(110, 62, 110, 1);
  -moz-box-shadow: 1px -4px 15px -1px rgba(110, 62, 110, 1);
  box-shadow: 1px -4px 15px -1px rgba(110, 62, 110, 1);
  }
}
</style>
