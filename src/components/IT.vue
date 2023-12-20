<template>
 <H1>it </H1>
  <div v-for="(employes, index) in IT" :key="index">
    <p>{{ employes.name }}</p>
    
  </div>
</template>
<script>
export default {
  name: "IT",
  props: ["IT"],
  methods:{
    deleteHr(name){
      this.$emit('delete',{name})
    }
  }
};
</script>
<style>
h1 {
  color: blue;
  padding: 50px;
  margin: 50px;
}
</style>
