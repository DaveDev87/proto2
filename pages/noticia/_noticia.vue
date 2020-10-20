<template>
  <div>
    <div v-if="isLoading">
      <h1>Cargando</h1>
    </div>
    <div v-else>
      <b-jumbotron>
        <h1>{{ this.news[0].titulo }}</h1>
        <h6>{{ this.news[0].autor }}</h6>
        <h6>{{ this.news[0].fecha }}</h6>
        <hr class="my-4" />
        <p>
          {{ this.news[0].contenido }}
        </p>
      </b-jumbotron>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      id: this.$route.params,
      news: [],
      isLoading: true
    };
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    filterData: function(id, datos) {
      return datos.filter(item => item.noticia === id);
    },
    fetchData: function() {
      axios
        .get(
          "https://5hg8ux24j8.execute-api.us-east-2.amazonaws.com/default/periodico"
        )
        .then(res => {
          const datos = res.data.Items;
          this.news = this.filterData(this.id.noticia, datos);
          this.isLoading = false;
        })
        .catch(err => console.log(err));
    }
  }
};
</script>

<style></style>
