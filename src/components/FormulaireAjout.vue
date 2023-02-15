<script lang="ts">
  export default {
    props: {
      taches: Object
    },
    methods: {
      ajouter(){
        this.taches.push({titre:this.titre,description:this.description})
      }
    },
    data() {
    	return {
				titre: "",
        description: ""
      }
    }
  }
</script>
<template>
  <hr>
  <label for="titre">Titre : </label>
  <input v-model="titre"  :id="titre">
  <br>
  <label :for="description"> Description : </label>
  <input v-model="description" :id="description"/>
  <br>
  <button @click="ajouter">Ajouter</button>
</template>