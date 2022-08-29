<script setup>
import ImageView from "./components/ImageView.vue";
import { ref, onMounted } from "vue";
import axios from "axios";
import Transcribe from "./components/Transcribe.vue";
import IconTranscribe from "./components/icons/IconTranscribe.vue";
const key_apod = import.meta.env.VITE_KEYAPOD;

let transcribe = ref(false);
let date = ref("");
const src = ref({});

const getApodData = async (now) => {
  const request = await axios.get(
    `https://api.nasa.gov/planetary/apod?api_key=${key_apod}&date=${now}`
  );

  date.value = request.data.date;
  src.value = request.data;
};

onMounted(async () => {
  const now = new Date();
  await getApodData(
    `${now.getFullYear()}-${now.getMonth() + 1}-${now.getDate()}`
  );
});
</script>

<template>
  <ImageView
    lang="en"
    v-if="transcribe === false"
    :content="src"
    role="ImageView"
  />
  <Transcribe
    lang="en"
    v-else
    :content="{ ...src, transcribe }"
    role="ImageExplanation"
  />
  <input type="date" lang="en-US" v-model="date" @change="getApodData(date)" />
  <button
    @click="transcribe ? (transcribe = false) : (transcribe = true)"
    :title="!transcribe ? 'Ler descrição' : 'Ver imagem/video'"
  >
    <IconTranscribe :transcribe="transcribe" />
  </button>
</template>

<style scoped lang="scss">
input {
  width: 100%;
  max-width: 320px;
  height: 60px;
  margin: auto;

  padding: 10px;
  font-size: 30px;

  position: relative;

  background: transparent;
  border: none;

  grid-row: 2/3;
  grid-column: 1/2;
}

button {
  width: 60px;
  height: 60px;
  margin: auto;

  border: none;
  background: transparent;
}
</style>
