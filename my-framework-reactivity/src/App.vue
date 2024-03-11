<script setup>
  import HelloWorld from './components/HelloWorld.vue';
  import { ref } from 'vue'


  const numCount = ref(0);
  const message = "SHOW SONGS";
  function increment() {
    numCount.value++
  }

const showText = ref(false);

function clickButton() {
  showText.value = !showText.value;
}
</script>
<template>
  <main>
    <section>
     <h2>Song Names</h2>
      <HelloWorld v-if="showText" />
      <button @click="clickButton"><slot>{{ message }}</slot></button>

    </section>


  </main>
  
</template>

<style scoped>
  main {
    display: flex;
    flex-direction: row;
  }

  button {
    cursor: pointer;
    margin-top: 22px;
    border: none;
    height: 7vh;
    width: 22vh;
    background: #4274ad;
    color: #bbcae9;
    font-weight: 900;
  }

  
</style>