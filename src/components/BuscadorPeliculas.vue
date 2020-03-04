<template>
  <div class="main">
    <b-container class="bv-example-row">
      <b-row>
        <b-col cols="1"></b-col>
        <b-col cols="10">
          <b-form inline>
            <label class="sr-only" for="input_pelicula_name">Pelicula</label>
            <b-input
                v-model="query"
                id="input_pelicula_name"
                class="mb-2 mr-sm-2 mb-sm-0"
                placeholder="Jane Doe"
            ></b-input>
            <b-button @click="hazQuery" variant="primary">Buscar</b-button>
            <b-button @click="ordenarPorAnio" variant="primary">Ordenar<b-button>
          </b-form>
        </b-col>
        <b-col cols="1"></b-col>
      </b-row>

      <b-row>
        <b-col cols="4" v-for="actual in results.Search" :key="actual.imdbID">
        </b-col>
      </b-row>
    </b-container>

  </div>
</template>

<script>
export default {
  data () {
    return{
      query:'',
      results:[],
      verDetalle:'',
      datalleResults:''
    }
  }
  methods:{
    hazQuery:function(){
      axios.get(`http://www.omdbapi.com/?apikey=19f8a30e&i=${this.query}`).then(response=>{ this.results=response.data;console.log(response)});

    },
    ordenarPorAnio:function(){

    },
    peticionDetalle:function(){

    })


  }
  name: 'BuscadorPeliculas',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
