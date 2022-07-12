<template>

  <section class="src-components-aplicacion">
   <div class="jumbotron">
    <h2> Ejercicio </h2>
    <hr>

     <div class="parrafo">
     Color: <input type="text" v-model="color"> 
     Fondo: <input type="text" v-model="backg"> 
     Size : <input type="text" v-model="size"> 
      <hr>
     Texto: <input :style="{color: color,
     background: backg, 
     fontSize: size}" 
     type="text" v-model.trim="text">

     <hr>

     Cantidad de Palabras: {{ cantPalabras }}
    </div>

    <br>
    <br>

    <h2> Respuestas </h2>
    <hr>
    <table class="table table-dark">
  <thead>
    <tr>
      <th scope="col">Número de Pregunta</th>
      <th scope="col">Respuesta</th>
    
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>B</td>
   </tr>
   <tr>
      <td>2</td>
      <td>C</td>
   </tr>
   <tr>
      <td>3</td>
      <td>B</td>
   </tr>
   <tr>
      <td>4</td>
      <td>D</td>
   </tr>
    <tr>
      <td>5</td>
      <td>D</td>
   </tr>
      
  </tbody>
</table>
  </div>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-components-aplicacion',
    props: [],
    mounted () {

    },
    data () {
     return {
        color: null,
        backg: null,
        size: null,
        text: " "
      }
    },
    methods: {

    },
    computed: {
      cantPalabras(){
        let cantidad=0 ;
        if (this.text != "" && (this.text.split(" ").length > 0)){
          let palabras=this.text.split(" ");
          cantidad = palabras.length;
        }
        return cantidad;
      }
    }
}


</script>

<style scoped lang="css">
  .jumbotron{
    background-color: rgb(196, 183, 183);
  }
</style>
