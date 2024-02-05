<script setup lang="ts">
</script>

<template>
  <svg viewBox="0 0 500 500">
    <path id="curve" d="M73,300 C173,181 334,188 436,300" />
    <text width="500">
      <textPath xlink:href="#curve">
        will you be my
      </textPath>
    </text>
  </svg>
  <img alt="heart" class="little-h" src="@/assets/whiteHeart.png" />
  <h1>valentine?</h1>
</template>

<style scoped>
textPath {
  text-transform: uppercase;
  font-size: 3.5rem;
  font-weight: bold;
}

svg {
  width: 20rem;
  position: absolute;
  top: 38%;
  left: 50%;
  transform: translate(-50%, -50%);
}

path {
  fill: transparent;
}

text {
  fill: #ffffff;
}

h1 {
  font-size: 5.5rem;
}

.little-h {
  margin: auto;
  display: block;
  margin-top: 7rem;
}
</style>