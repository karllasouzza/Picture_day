<script setup>
defineProps({ content: Object });
</script>
<template>
  <figure>
    <img
      v-if="content.media_type === 'image'"
      :src="content.hdurl"
      :alt="content.explanation"
    />
    <iframe
      lang="en-US"
      :src="content.url"
      frameborder="0"
      allowfullscreen
      v-else
      :longdesc="content.title"
    ></iframe>
  </figure>
</template>

<style lang="scss" scoped>
img,
iframe {
  width: 100%;
  height: 100%;

  object-fit: cover;
}

figure {
  width: 100%;
  height: 100%;

  grid-row: 1/2;
  grid-column: 1/3;

  overflow: hidden;

  border-radius: 0 0 1.5rem 1.5rem;
}
</style>
