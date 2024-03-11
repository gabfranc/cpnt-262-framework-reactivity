<script setup>

import '../assets/main.css'
import { reactive } from "vue"

const artist = reactive({
  name: "Taylor Swift",
  songs: [
    "Our Song",
    "Illicit Affairs",
    "Cornelia Street",
    "Paris",
    "I Did Something Bad",
    "Mean~ Taylor's Version",
    "I Knew Places~Taylor's Version",
    "Red~Taylor's Version"
  ]
})


</script>

<template>
  <section>
    <div>
      <h4>{{ artist.name }}</h4>
    </div>
      <ul>
        <li v-for="(song, index) in artist.songs" :key="index">
          <span v-bind:class="{active: song.isActive}">
            <a href="https://open.spotify.com/artist/06HL4z0CvFAxyc27GXpf02?si=aVPzFAH0Txmybdcb5qgJvw">{{ song }}</a>
          </span>
        </li>
      </ul>
    
   </section>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
