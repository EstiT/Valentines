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
let pad = 0;
const padding = ref('0 1rem');

function hover($event: Event) {
  const min = -9;
  const max = 9;
  const translate = `translate(${Math.ceil(Math.random() * (max + 2 - min + 2) + min + 2)}rem, ${Math.ceil(Math.random() * (max - min) + min)}rem)`
  if ($event.target) {
    ($event.target as HTMLElement).style.transform = translate;
  }
  padding.value = `${pad}rem ${pad + 1}rem`
  pad += 0.5;
}
</script>

<template>
  <main>
    <Question />
    <div class="buttons">
      <RouterLink to="/yes" class='lined thin yesBtn'>Yes!</RouterLink>
      <RouterLink to="/" class='lined thin noBtn' @mouseover="hover">{{ phrases[phraseIndex] }}</RouterLink>
    </div>
    <img src="@/assets/pusheenHeart.gif" class="pusheen" />
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

.pusheen {
  position: absolute;
  right: 22%;
  top: 15%;
  width: 8rem;
  object-fit: contain;
}

.yesBtn {
  padding: v-bind(padding);
}

.noBtn {
  position: relative;
  z-index: 2;
}
</style>