<template>
  <div class="title flex-centered" :class="{ checked: atividade.checked }"></div>
    <div class="title-content">
      <div class="title-subtitle">{{ atividade.description }}</div>
      <div>{{ atividade.checked }}</div>
    </div>
    <div class="title-action">
      <button @click="$emit('toggle', atividade)" class="btn btn-primary">
        Concluido
        <span v-if="atividade.checked">Desmarcar</span>
        <span v-else>Concluido</span>
      </button>
      <button class="btn btn-error">Remover</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Lista",

  props: {
    atividade: { type: Object, required: true },
  },
};
</script>

<style scoped>
.checked {
  text-decoration: line-through;
  color: lightslategray;
}
</style>