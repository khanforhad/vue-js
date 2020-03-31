<template>
<header>
    <h1 v-on:click="changeTitle">{{title}}</h1>
</header>
</template>

<script>
import {bus} from '../main'
export default {
  props:{
    title:{
      type:String
    }
  },
  data () {
    return {
      
    }
  },
  methods:{
    changeTitle:function(){
      //this.$emit('changeTitle','Forhad Khan');
      this.title ='Forhad Khan';
      bus.$emit('titleChanged','Forhad Khan');

    }
  }
}
</script>

<style scoped>
header{
    background: lightgreen;
    padding: 10px;
}
h1{
    color:#222;
    text-align: center;
}
</style>
