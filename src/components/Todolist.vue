<template>
  <div class="principal">
    <div class="board">
      <div class="pendente">
        <h3>Pendente</h3>
        <div class="card">
          <div class="atividade-main">
            <div class="atividade">atividade</div>
            <div class="content" contenteditable="true">123</div>
            <div class="img" img src="">001</div>
            <div class="butons">
              <button id="play">play</button>
              <button id="coment">coment</button>
              <button id="config">config</button>
              <div class="timer-container">
                <div class="timer-display">00:00:00</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="board">
      <div class="pendente">
        <h3>Pendente</h3>
        <div class="card">
          <div class="atividade-main">
            <div class="atividade">atividade</div>
            <div class="content" contenteditable="true">123</div>
            <div class="img" img src="">001</div>
            <div class="butons">
              <button id="play">play</button>
              <button id="coment">coment</button>
              <button id="config">config</button>
              <div class="timer-container">
                <div class="timer-display">00:00:00</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="board">
      <div class="pendente">
        <h3>Pendente</h3>
        <div class="card">
          <div class="atividade-main">
            <div class="atividade">atividade</div>
            <div class="content" contenteditable="true">123</div>
            <div class="img" img src="">001</div>
            <div class="butons">
              <button id="play">play</button>
              <button id="coment">coment</button>
              <button id="config">config</button>
              <div class="timer-container">
                <div class="timer-display">00:00:00</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="board">
      <div class="pendente">
        <h3>Pendente</h3>
        <div class="card">
          <div class="atividade-main">
            <div class="atividade">atividade</div>
            <div class="content" contenteditable="true">123</div>
            <div class="img" img src="">001</div>
            <div class="butons">
              <button id="play">play</button>
              <button id="coment">coment</button>
              <button id="config">config</button>
              <div class="timer-container">
                <div class="timer-display">00:00:00</div>
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
  name: "Todolist",
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
  display: flexbox;
  position: relative;
  background: #fff;
  border-radius: 5px;
}

.card {
  position: relative;
  display: block;
  justify-content: space-around;
  flex-direction: row;
  height: 250px;
  weight: 250px;
  background: #d4caca;
}
.pendente {
  display: block;
  justify-content: space-between;
  height: 300px;
  weight: 25px;
  background: blue;
  border-radius: 5px;
}
.execucao {
  display: block;
  justify-content: space-between;
  height: 300px;
  weight: 25px;
  background: tomato;
  border-radius: 5px;
}

.atrasadas {
  display: block;
  justify-content: space-between;
  height: 300px;
  weight: 25px;
  background: red;
  border-radius: 5px;
}

.concluidas {
  display: block;
  justify-content: space-between;
  height: 300px;
  weight: 25px;
  background: green;
  border-radius: 5px;
}
.h3 {
  color: black;
  padding: 16px;
}

.atividade {
  justify-content: space-between;
  display: flex;
}

.descricao {
}
</style>