<template>
  <AtivForm />
  <Todolist />
  <Atividades />
</template>

<script>
// import AtivForm from '../src/components/AtivForm.vue'
import Todolist from "../src/components/Todolist.vue";
import Atividades from "../src/components/Atividades.vue";

export default {
  name: "App",
  components: {
    // AtivForm,
    Todolist,
    Atividades,
  },
};
</script>

<style>
</style>
