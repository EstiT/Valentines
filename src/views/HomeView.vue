<script setup lang="ts">
import { RouterLink } from 'vue-router';
import { ref } from 'vue';
import Question from '../components/Question.vue';

const noCopy = ref('No');
</script>

<template>
  <main>
    <Question />
    <RouterLink to="/">Yes</RouterLink>
    <RouterLink to="/about">{{ noCopy }}</RouterLink>
    <img alt="heart" class="heart h1" src="@/assets/heart.svg" width="850" height="850" />
    <img alt="heart" class="heart h2" src="@/assets/heart.svg" width="850" height="850" />
  </main>
</template>