<template>
  <h1>HR</h1>
  <div class="hr-date">
    <div v-for="(employes, index) in HR" :key="index">
      <p>
        <span>{{ employes.name }}</span>
        <span><button @click="deleteHr(employes.name)">Delete</button></span>
      </p>
    </div>
  </div>
</template>
<script>
export default {
  name: "HR",
  props: ["HR"],
  created()
  {
    alert("crate")
  },
  beforeCreate()
  {
    alert("last create")
  }
  methods: {
    deleteHr(name) {
      this.$emit("delete", name );
    },
  },
};
</script>
<style>
h1 {
  color: blue;
}
</style>
