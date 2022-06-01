<template>

    <div class="tile flex-centured" :class="{ checked: atividade.checked}">

        <dir class="tile-content">

            <div class="tile-subtitle">  {{ atividade.description }}</div>
            

        </dir>

        <div class="tile-action">

            <button @click="$emit('toggle', atividade)" class="btn btn-primary"> 
                <span v-if="atividade.checked"> Desmarcar </span>
                <span v-else> Concluido </span>
                
                
            </button>

            <button @click="$emit('remove', atividade)" class="btn btn-error"> Remover  </button>




        </div>


    </div>
    
</template>


<script>
    export default {
        name: "Atividade",
        props: {
            atividade: { type: Object, required: true}
        }
    };
</script>


<style scoped>
    .checked {
        text-decoration: line-through;
        color: lightslategray;
    }
</style>