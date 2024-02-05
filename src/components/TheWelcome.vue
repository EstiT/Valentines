<script setup lang="ts">
</script>

<template>
  <svg viewBox="0 0 500 500">
    <path id="curve" d="M73.2,148.6c4-6.1,65.5-96.8,178.6-95.6c111.3,1.2,170.8,90.3,175.1,97" />
    <text width="500">
      <textPath xlink:href="#curve">
        will you be my
      </textPath>
    </text>
  </svg>
  <h1>valentine?</h1>
</template>

<style scoped>
textPath {
  text-transform: uppercase;
  font-size: 3.25rem;
  font-weight: bold;
}

path {
  fill: transparent;
}

text {
  fill: #ffffff;
}
</style>