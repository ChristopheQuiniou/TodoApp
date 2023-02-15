<script lang="ts">
	export default {
    props: {
      titre: String,
      description: String
  	}
  }
</script>

<template>
  <div :style="{'background-color': 'rgb(247, 171, 46)'}">
    <h2>
    	{{titre}}
    </h2>
    <p>
      {{description}}
    </p>
  </div>
  
</template>