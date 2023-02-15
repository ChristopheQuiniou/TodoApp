<script>
  import Tache from "./components/Tache.vue"
  import FormulaireAjout from "./components/FormulaireAjout.vue"
  
  export default {
    components: {
      Tache,
      FormulaireAjout
    },
    data(){
      return{
        taches: [{titre:"ff",description:"la description"}]
      }
    }
  }
</script>

<template>
  <h1>
    TodoApp
  </h1>
  <p v-if="taches.length == 0">
    Ma liste de tâches est vide 😊
  </p>
	<Tache v-for="tache in taches" :titre="tache.titre" description="tache.description"/>
  <FormulaireAjout taches="taches"/>
</template>