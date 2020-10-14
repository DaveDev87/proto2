<template>
  <b-card :title="newsData.title" :sub-title="newsData.author">
    <b-card-text>
      {{ newsData.body }}
    </b-card-text>
    <nuxt-link :to="`/noticia/${newsData.id}`">
      Seguir leyendo
    </nuxt-link>
  </b-card>
</template>

<script>
export default {
  props: ["newsData"]
};
</script>

<style></style>
