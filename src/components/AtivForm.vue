<template>
    <div>
        <div><!-- formulário,arrumar para separar os compo        <div>nentes depois -->
            <form id="ativi-form" @submit="createTarefa">
            <div class="input-container">
                <label for="nome">Nome da Atividade:</label>  
                <input type="text" id="nome" name="nome" v-model="nome" placeholder="Digite o nome da atividade">
            </div>
                <div class="input-container">
                <label for="atribuir">Atribuir a:</label>
                    <select name="colaborador" id="colaborador" v-model="colaborador">
                    <option v-for="colaborador in colaboradores" :key="colaborador.id" :value="colaboradores.tipo">
                        {{colaboradores.tipo}}
                    </option>
                    </select>
            </div>
            <div class="input-container">
                <label for="type">Tipo de atividade :</label>
                    <select name="tipo" id="tipo" v-model="tipo">
                        <option v-for="tipo in tipos" :key="tipo.id" value="tipos.tipo">
                        {{tipos.tipo}}
                        </option>
                    </select>
            </div>
                <div class="input-container">
                <label for="priority">Nível de prioridade:</label>
                    <select name="prioridade" id="prioridade" v-model="prioridade">
                        <option v-for="prioridade in prioridades" :key="prioridade.id" :value="prioridades.tipo">
                        {{prioridades.tipo}}
                        </option>
                    </select>
                </div>
                <div class="input-container">
                <label for="inicio">Inicio em:</label>  
                <input type="text" id="inicio" name="inicio" v-model="inicio" placeholder="Data de início">
                </div>
                <div class="input-container">
                <label for="final">Finaliza em:</label>  
                <input type="text" id="final" name="final" v-model="final" placeholder="Data de finalização">
                </div>
                <div class="input-container">
                <label for="descricao">Descrição:</label>  
                <input type="text" id="descricao-box" name="descricao" v-model="descricao" placeholder="Descrição">
                </div>
                <div class="input-container">
                <input type="submit" class="submit-btn" value="Enviar atividade">
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name:"AtivForm",
   //parei aqui no backend dos "ingredientes do video",cadastrar no db.jsonn
    data() {
        return {
            colaboradores:null,
            tipos:null,
            prioridades:null,
            nome:null,
            inicio:null,
            final:null,
            descricao:null,
            msg:null
        }
    },
<<<<<<< HEAD
    methods: {
     async getActivities(){
            const req = await fetch("http://localhost:3000/Activities");
            const data = await req.json();

            this.tipos= data.tipos;
            this.colaboradores = data.colaboradores;
            this.prioridades = data.prioridades;
        },
        async createTarefa(e){
            
            e.preventDefault();

            const data = { 
                colaboradores: this.colaboradores,
                tipos: this.tipos,
                prioridades: this.prioridades,
                status:"Em aberto"
            }
           
           const dataJson = JSON.stringify(data);

           const req = await fetch("http://localhost:3000/tarefas", {
               method: "POST",
               headers:{"Content-Type":"application/json"},
               body:dataJson
           });
           
        //    const res = await req.json();
           this.colaboradores="";
           this.tipos="";
           this.prioridades="";

        }
    },
    mounted(){
     this.getActivities()
   }
=======
    //  methods: {
    //      async getActivities(){
            
    //         // const req = await fetch("http://localhost:3000/Activities");
    //         const data = await req.json();

    //         console.log(data);
    //     }
    // },
    // mounted(){
    //     this.getActivities()
    // }
>>>>>>> 2d82f1ed703363d25ca3fe7649553a64475d6206
}

</script>

<style scoped>
   /* stilo do formulário */
   #ativi-form {
        max-width: 400px;
        margin: 0 auto;
        content: justify-content;
    }

    .input-container {
        display: flex;
        flex-direction:column;
        margin-bottom: 20px; 
        max-width: 400px;
        margin-left:5%;
        padding: 10px;
        transition: 0.5s;
    }

    label {
        font-weight: bold;
        margin-bottom: 15px;
        color: #222;
        padding: 5px 10px;
        border-left: 4px solid #fcba03;
    }

    input.select{
        padding:5px 10px;
        width:300px;
    }
/* ajustar a descrição  */
    .descricao-box {
        display: flex;
        flex-direction: column;
        margin-bottom: 20px; 
        min-width: 200px;
        min-height:150px;
        margin-left:5%;
        padding: 0;
    }
/* arrumar o botão enviar */
    .submit-btn { 
        background-color: #222;
        color:#fcba03;
        font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        margin:0 auto;
        cursor:pointer;
        transition:.5s;
    }

    .submit-btn:hover {
        background-color: transparent;
        color:#222;
    }
</style>
