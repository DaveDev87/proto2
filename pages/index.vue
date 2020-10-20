<template>
  <div>
    <div v-for="item in news" class="card" :key="item.id">
      <CardNoticia :news-data="item" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      news: []
    };
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    fetchData: function() {
      axios
        .get(
          "https://5hg8ux24j8.execute-api.us-east-2.amazonaws.com/default/periodico"
        )
        .then(res => {
          const datos = res.data.Items;
          this.news = datos;

          // setdata(filterData(id, datos));
          // setisLoading(false);
        })
        .catch(err => console.log(err));
    }
  }
};
</script>

<style scoped>
.card {
  width: 64rem;
  margin: 10px auto 10px auto;
}
</style>
