<template>
  <div class="principal">
        <div class="board">
             <div class="pendente">
                 <h3>Pendente</h3>
                 <div class="card">
                    <div class="atividade-main">
                        <div class="atividade">atividade</div>
                        <div class="content" >123</div>
                        <div class="button-container">
                           <div class="butons">
                               <!-- ajustar o tamanho das imagens
                               <img src="../assets/play.png" id="play">
                                <img src="../assets/comentar.png" id="coment">
                                <img src="../assets/options.png" id="options">
                                -->
                                <div class="timer-display">
                                    <div class="timer">
                                        00:00:00
                                    </div>
                                </div>
                           </div>
                        </div>
                    </div>
                 </div>
             </div>
        </div>
        <div class="board">
             <div class="execucao">
                 <h3>Em Execução</h3>
                 <div class="card">
                    <div class="atividade-main">
                        <div class="atividade">atividade</div>
                        <div class="content" >123</div>
                        <div class="button-container">
                           <div class="butons">
                               <!-- ajustar o tamanho das imagens
                               <img src="../assets/play.png" id="play">
                                <img src="../assets/comentar.png" id="coment">
                                <img src="../assets/options.png" id="options">
                                -->
                                <div class="timer-display">
                                    <div class="timer">
                                        00:00:00
                                    </div>
                                </div>
                           </div>
                        </div>
                    </div>
                 </div>
             </div>
        </div>
        <div class="board">
             <div class="atrasadas">
                 <h3>Atrasadas</h3>
                 <div class="card">
                    <div class="atividade-main">
                        <div class="atividade">atividade</div>
                        <div class="content" >123</div>
                        <div class="button-container">
                           <div class="butons">
                               <!-- ajustar o tamanho das imagens
                               <img src="../assets/play.png" id="play">
                                <img src="../assets/comentar.png" id="coment">
                                <img src="../assets/options.png" id="options">
                                -->
                                <div class="timer-display">
                                    <div class="timer">
                                        00:00:00
                                    </div>
                                </div>
                           </div>
                        </div>
                    </div>
                 </div>
             </div>
        </div>
        <div class="board">
             <div class="concluidas">
                 <h3>Concluidas</h3>
                 <div class="card">
                    <div class="atividade-main">
                        <div class="atividade">atividade</div>
                        <div class="content" >123</div>
                        <div class="button-container">
                           <div class="butons">
                               <!-- ajustar o tamanho das imagens
                               <img src="../assets/play.png" id="play">
                                <img src="../assets/comentar.png" id="coment">
                                <img src="../assets/options.png" id="options">
                                -->
                                <div class="timer-display">
                                    <div class="timer">
                                        00:00:00
                                    </div>
                                </div>
                           </div>
                        </div>
                    </div>
                 </div>
             </div>
        </div>
  </div>
</template>

<script>
export default {
    name: "Lista",
};
</script>

<style scoped>
.board {
  background-color: #f1f1f1;
  width: 100%;
  margin: 5px;
}

.principal {
  display: flex;
  background-color: #f1f1f1;
  width: 100%;
  margin: 5px;
}

.atividade-main {
  display: block;
  background: #fff;
  border-radius: 5px;
  width: 235px;
  height: 100px;
}

.card {
  display: flex;
  justify-content: space-around;
  flex-direction: row;
  height: 250px;
  width: 250px;
  background: #d4caca;
}
.pendente {
  display: block;
  justify-content: space-between;
  height: 300px;
  width: 250px;
  background: blue;
  border-radius: 5px;
}
.execucao {
  display: block;
  justify-content: space-between;
  height: 300px;
  width: 250px;
  background: tomato;
  border-radius: 5px;
}

.atrasadas {
  display: block;
  justify-content: space-between;
  height: 300px;
  width: 250px;
  background: red;
  border-radius: 5px;
}

.concluidas {
  display: block;
  justify-content: space-between;
  height: 300px;
  width: 250px;
  background: green;
  border-radius: 5px;
}
.h3 {
  color: black;
  padding: 16px;
  font-weight: bold;
  margin-left: 45px;
}

.atividade {
  justify-content: space-between;
  display: flex;
}

.timer-display {
  display:flex;
  justify-content:space-around;
  color: white;
  background-color: red;
  margin-left: 140px;
  margin-right: 8px;
  border: double;
  border-radius: 5px;
}

.content{
    background-color: #f1f1f1;
    border:black;
    border-radius:5px;
    width:99%;
    max-height: 40px;
    margin-left: 3px;
    margin-right: 3px;
}

.atividade{
    margin-left: 3px;
    margin-right: 3px;
    color:black;
    font-weight: bold;
}
.buttons{
  display:flex;
  padding: 5%;
}

.play{
    max-width: 20px;
}
</style>