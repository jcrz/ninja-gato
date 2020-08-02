<template>
  <div class="container">
    <b-row>
      <b-col cols="6">
        <b-button variant="success" @click="mostrarNinja()">Ninja</b-button>
      </b-col>
      <b-col cols="6">
        <b-button variant="success" @click="mostrarGato()">Gato</b-button>
      </b-col>
      <b-col cols="12">
        <img v-bind:src="require('../assets/'+img)" alt="imagen">
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: function() {
    return {
      img: 'logo.png'
    }
  },
  methods: {
    mostrarNinja(){
      this.img = 'ninja.jpeg'
    },
    mostrarGato(){
      this.img = 'gato.jpg'
    }
  },
  beforeUpdate(){
    alert('La imagen cambiará.')
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  width: 500px;
}
</style>
