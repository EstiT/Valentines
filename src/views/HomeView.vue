<script setup lang="ts">
import { RouterLink } from 'vue-router';
import { ref } from 'vue';
import Question from '../components/Question.vue';


const phraseIndex = ref(0);
const phrases = [
  'No',
  'Are you sure?',
  'Really sure?',
  'Think again',
  'Last chance',
  'Surely not',
  'You might regret this',
  'Give it some more thought',
  'Are you absolutely sure?',
  'This could be a mistake',
  'Have a heart',
  "Wouldn't recommend",
  "Is that you final answer?",
  "You're breaking my heart"
];

function hover($event: Event) {
  const min = -30;
  const max = 20;
  const translate = `translate(${Math.ceil(Math.random() * (max - min) + min)}rem, ${Math.ceil(Math.random() * (max - min) + min)}rem)`
  if ($event.target) {
    ($event.target as HTMLElement).style.transform = translate;
  }
}
</script>

<template>
  <main>
    <Question />
    <div class="buttons">
      <RouterLink to="/" class='lined thin'>Yes!</RouterLink>
      <RouterLink to="/about" class='lined thin noBtn' @mouseover="hover">{{ phrases[phraseIndex] }}</RouterLink>
    </div>
    <img alt="heart" class="heart h1" src="@/assets/heart.svg" width="850" height="850" />
    <img alt="heart" class="heart h2" src="@/assets/heart.svg" width="850" height="850" />
  </main>
</template>

<style scoped>
.buttons {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>