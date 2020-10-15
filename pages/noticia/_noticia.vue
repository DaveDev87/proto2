<template>
  <div >
  <b-jumbotron v-for="product in getData($route.params.noticia)" :key="product.id">
    <template v-slot:header>
      <p>{{ product.title }}</p>
    </template>

    <template v-slot:lead >
      {{product.author}} in {{product.createdAt}}
    </template>

    <hr class="my-4">

    <p>
      {{product.body}}
    </p>

    <img src="https://preview.redd.it/etimc4de4xp51.jpg?auto=webp&s=db7d863ce4d9f2b5ade299d0c6600470aa6a155f" class="img-fluid" alt=""/>
  </b-jumbotron>
  </div>
</template>

<script>
export default {
  created(){
    console.log(this.$route.params.noticia)
  },
  data() {
    
      return {
        id: this.$route.params,
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
        
      }
    },
    methods: {
    getData(id) {
      const data = this.news
      return data.filter(item => {
        return item.id == id
      })
    }
  }

  
};

</script>

<style></style>
