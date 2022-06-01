<template>
  <Atividades />

  <div id="Todolist">
    <div class="container">
      <form @submit.prevent="addAtividade(atividade)">
        <div class="input-group">
          <!-- deixar na mesma linha -->
          <input
            type="text"
            v-model="atividade.description"
            class="form-input"
            placeholder="Nome da atividade"
          />
          <!--  -->
          <button class="btn btn-primary">
            <i class="icon icon-plus"></i>
          </button>
        </div>
        <ul class="step">
          <li class="step-item active">
            <a href="#" class="tooltip" data-tooltip="Step 1">Passo 1</a>
          </li>
          <li class="step-item">
            <a href="#" class="tooltip" data-tooltip="Step 2">Passo 2</a>
          </li>
          <li class="step-item">
            <a href="#" class="tooltip" data-tooltip="Step 3">Passo 3</a>
          </li>
          <li class="step-item">
            <a href="#" class="tooltip" data-tooltip="Step 4">Passo 4</a>
          </li>
        </ul>
      </form>
      <!-- deixar na mesma linha -->
      <div class="tarefa list">
        <atividade
          v-for="a in atividades"
          :key="a.id"
          @toggle="toggleAtividade" 
          @remove="removeAtividade"
          :atividade="a"
        ></atividade>
        <!--  -->
      </div>
    </div>
  </div>
</template>


<script>
import Atividades from "./Atividades.vue"

export default {
  name: "Todolist",
  components: {
    Atividades,
  },

  data() {
    return { atividades: [], atividade: { checked: false } };
  },

  methods: {
    addAtividade(atividade) {
      atividade.id = Date.now();
      this.atividades.push(atividade);
      this.atividade = { checked: false };
    },

    toggleAtividade(atividade) {
      const index = this.atividades.findIndex(
        (item) => item.id === atividade.id
      );
      if (index > -1) {
        const checked = !this.atividades[index].checked;
        this.atividades[index].checked = checked;
      }
    },
    
    removeAtividade(atividade){
      
      const index = this.atividades.findIndex((item) => item.id === atividade.id);
      if (index > -1) {

        this.atividades.splice(index,1);

    }
  },
};
</script>

<style scoped>
.atividade-list {
  padding: 10px;
}
</style>