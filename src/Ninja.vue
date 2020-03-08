<template>
  <div id="app">
    <ul>
    	<li v-for="ninja in ninjas">
    		{{ninja}}
    	</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      ninjas: ['Forhad','Afsana','Afsar']
    }
  }

}
</script>
