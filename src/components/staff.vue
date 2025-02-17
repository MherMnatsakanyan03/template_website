<script setup>
import { ref } from 'vue'

const images = ref([
  { src: 'src/assets/staff/ComfyUI_00002_.png', text: 'Staff Member 1' },
  { src: 'src/assets/staff/ComfyUI_00007_.png', text: 'Staff Member 2' },
  { src: 'src/assets/staff/ComfyUI_00008_.png', text: 'Staff Member 3' },
  // Add more images and text as needed
])
</script>

<template>
  <div class="scroll-container">
    <div class="scroll-content" v-for="(image, index) in images" :key="index">
      <img :src="image.src" alt="" />
      <p>{{ image.text }}</p>
    </div>
  </div>
</template>

<style scoped>
.scroll-container {
  display: flex;
  overflow-x: auto;
  white-space: nowrap;
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  background-color: #f0f0f0;
  border-radius: 10px;
}

.scroll-content {
  display: inline-block;
  text-align: center;
  margin: 0 10px;
}

.scroll-content img {
  width: 150px;
  height: 150px;
  object-fit: cover;
  border-radius: 50%;
}

.scroll-content p {
  margin-top: 5px;
  font-size: 14px;
  color: #555;
}
</style>
