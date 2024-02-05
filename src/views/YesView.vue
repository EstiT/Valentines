<template>
  <div class="yes">
    <h1>Ok yay</h1>
    <img src="@/assets/pusheenHug.gif" class="pusheen" />
    <img alt="heart" class="heart h1" src="@/assets/heart.svg" width="850" height="850" />
    <img alt="heart" class="heart h2" src="@/assets/heart.svg" width="850" height="850" />
  </div>
</template>

<style scoped>
.yes {
  min-height: 100vh;
  display: flex;
  align-items: center;
}

.pusheen {
  position: absolute;
  right: 8%;
  top: 10%;
  width: 22rem;
  object-fit: contain;
}
</style>
