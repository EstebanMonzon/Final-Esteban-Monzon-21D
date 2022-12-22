<template >
  <section>
    <div class="jumbotron">
      <h2>Temperatura</h2>
      <label for="">Ingrese Temperatura en C°</label>
      <input type="number" v-model="Centrigrados">
      <p >Valor convertido Farenheit <span :style="getEstilos(this.Centrigrados)">{{ TemperaturaFarenheit =  (this.Centrigrados * FarenheitCalculo) + FarenheitSuma}}</span> </p>
      <p >Valor convertido Kelvin <span :style="getEstilos(this.Centrigrados)">{{ TemperaturaKelvin = (this.Centrigrados * 1) + kelvinSuma }}</span> </p>
      <hr />
      <br />
    </div>

    <div>
      <h2>Respuestas</h2>
      <table class="table">
        <thead>
          <tr>
            <th scope="col">Pregunta</th>
            <th scope="col">Respuesta</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1_Como es la forma reducida de v-on:click?</td>
            <td>C</td>
          </tr>
          <tr>
            <td>2_vue create se utiliza para:</td>
            <td>B</td>
          </tr>
          <tr>
            <td>3_El modificador trim recorta...</td>
            <td>C</td>
          </tr>
          <tr>
            <td>
              4_La propiedad routes en la definición del router de Vue.js tiene
              como función:
            </td>
            <td>A</td>
          </tr>
          <tr>
            <td>5_Las mutaciones contienen...</td>
            <td>C</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<script >
export default {
  name: "src-componentes-usuarios",
  props: [],
  mounted() {
  },
  data() {
    return {
      Centrigrados: 0,
      FarenheitCalculo: 1.8,
      FarenheitSuma: 32,
      kelvinSuma: 273.15
    };
  },
  methods: {
    getEstilos(){
      if(this.Centrigrados <= 0){
        return {color: 'blue'} 
      }
      if(this.Centrigrados > 0 && this.Centrigrados < 15){
        return {color: 'magenta'} 
      }
      else{
        return {color: 'red'} 
      }
    }
      
  },
  computed: {},
};
</script>

<style scoped lang="css">
h2 {
  text-align: center;
}
</style>
