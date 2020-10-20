<template>
  <b-card :title="newsData.titulo" :sub-title="newsData.autor">
    <b-card-text>
      {{ newsData.contenido }}
    </b-card-text>
    <nuxt-link :to="`/noticia/${newsData.noticia}`">
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
