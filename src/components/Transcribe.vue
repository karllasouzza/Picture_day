<script setup>
defineProps({ content: Object });
</script>

<template>
  <article>
    <h1 lang="en">{{ content.title }}</h1>
    <p lang="en">{{ content.explanation }}</p>
  </article>
</template>

<style lang="scss" scoped>
article {
  width: 100%;
  height: 100%;
  padding: 10px;

  grid-row: 1/2;
  grid-column: 1/3;

  display: flex;
  flex-direction: column;

  overflow: auto;
  border-radius: 0 0 1.5rem 1.5rem;

  h1 {
    font-size: 1.5em;
    text-align: start;
    line-height: 1.1;

    margin: 15px 0;
  }

  p {
    font-size: 1.1em;
    text-align: start;
  }
}
</style>
