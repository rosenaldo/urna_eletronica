<template>
  <div id="app">
    <div class="urna">
      <tela :tela="tela" />
      <teclado />
    </div>
  </div>
</template>

<script>
import "@/css/global.css";
import teclado from "@/components/urna-teclado.vue";
import tela from "@/components/urna-tela.vue";

export default {
  name: "App",
  components: {
    tela,
    teclado,
   
  },
  date() {
    return {
      tela: "prefeito",
    };
  },
};
</script>

<style>
#app {
  background-color: var(--background-color);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.urna {
  width: 1000px;
  height: 500px;
  background-color: var(--ballot-box-background-color);
  padding: 30px;
  border-radius: 5px;
  display: flex;
  justify-content: space-between;
}
</style>
