<template>
    <div>
      <h1>Fabric.js</h1>

      <canvas ref="canvas" width="600" height="400"></canvas>
    </div>
  </template>
  
  <script setup>
  import { onMounted, ref } from 'vue';
  import * as fabric from 'fabric';
 
  const canvasRef = ref(null);
  
  onMounted(() => {
    
    const canvas = new fabric.Canvas(canvasRef.value);
  
    
    fabric.Image.fromURL('https://images.pexels.com/photos/271649/pexels-photo-271649.jpeg?auto=compress&cs=tinysrgb&w=600', function (img) {
      img.scale(0.5);
      canvas.add(img);
      canvas.renderAll();
    });
  });
  </script>
  
  <style lang="scss" scoped>
  canvas {
    border: 1px solid #ccc;
    height: 30.75rem;
    width: 30.5rem;
    
  }
  </style>
  