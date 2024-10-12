<template>
  <div>
    <h1>Fabric.js</h1>

    <canvas ref="canvas"></canvas>
  </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
// import * as fabric from "fabric";
// import { fabric } from 'fabric';
import fabric

const canvasRef = ref(null);

onMounted(() => {
  const canvas = new fabric.Canvas(canvasRef.value);
  fabric.Image.fromURL(
    "https://images.pexels.com/photos/271649/pexels-photo-271649.jpeg?auto=compress&cs=tinysrgb&w=600",
    function (img) {
      img.set({
        height: "10rem",
        width: "10rem",
      });
      canvas.setBackgroundImage(img,()=>{
        canvas.renderAll()
      })
    }
  );
});
</script>

<style lang="scss" scoped>
canvas {
  border: 1px solid #ccc;
  height: 30.75rem;
  width: 30.5rem;
  border-radius: 1rem;
  -webkit-box-shadow: 1px -4px 15px -1px rgba(110, 62, 110, 1);
  -moz-box-shadow: 1px -4px 15px -1px rgba(110, 62, 110, 1);
  box-shadow: 1px -4px 15px -1px rgba(110, 62, 110, 1);
}
</style>
