<template>
  <div>
    <div v-for="item in news" class="card" :key="item.id">
      <CardNoticia :news-data="item" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      news: [
        {
          id: 1,
          title: "titulo1",
          body:
            "dew dew dew dw de wd we dwed we de wd  erv f  v r ef erf er fer f erfe",
          author: "Juanito Alcachofa",
          createdAt: "2020-12-03",
          updatedAt: "2020-10-23"
        },
        {
          id: 2,
          title: "titulo2",
          body:
            "dew dew dew dw de wd we dwed we de wd  erv f  v r ef erf er fer f erfe",
          author: "Juanito Alcachofa",
          createdAt: "2020-12-03",
          updatedAt: "2020-10-23"
        },
        {
          id: 3,
          title: "titulo3",
          body:
            "dew dew dew dw de wd we dwed we de wd  erv f  v r ef erf er fer f erfe",
          author: "Juanito Alcachofa",
          createdAt: "2020-12-03",
          updatedAt: "2020-10-23"
        },
        {
          id: 4,
          title: "titulo4",
          body:
            "dew dew dew dw de wd we dwed we de wd  erv f  v r ef erf er fer f erfe",
          author: "Juanito Alcachofa",
          createdAt: "2020-12-03",
          updatedAt: "2020-10-23"
        }
      ]
    };
  }
};
</script>

<style scoped>
.card {
  width: 64rem;
  margin: 10px auto 10px auto;
}
</style>
