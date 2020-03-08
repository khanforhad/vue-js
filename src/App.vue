<template>
<div>
  <app-header></app-header>
  <app-ninjas v-bind:ninjas="ninjas"></app-ninjas>
  <app-footer></app-footer>
</div>
</template>

<style scoped>

</style>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Ninjas from './components/Ninja.vue';

export default {
  components:{
    'app-header':Header,
    'app-footer':Footer,
    'app-ninjas':Ninjas,
  },
  name: 'app',
  data () {
    return {
      ninjas:[
          {name:'Forhad', speciality:'Vue Js', show:false},
          {name:'Robin', speciality:'Doctor', show:false},
          {name:'Mishu', speciality:'Mathmitics', show:false},
          {name:'Afsana', speciality:'Writer', show:false},
          {name:'Sumon', speciality:'Artiest', show:false},
          {name:'Jamal', speciality:'Dancer', show:false}
      ]
    }
  }

}
</script>
