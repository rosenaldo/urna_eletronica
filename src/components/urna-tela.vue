<template>
  <div class="urna-tela">
    <div v-if="tela != 'fim'" class="urla-tela-voto">
    <div class="urna-tela-voto-textos">
        <div class="urna-tela-voto-titulo">Seu voto para:</div>
        <div class="urna-tela-voto-tipo">{{tela}}</div>
    </div>
    <div class="urna-tela-voto-imagem"></div>
    <div class="urna-tela-voto-instrucoes"></div>
    
    
    </div>
  <div v-if="tela == 'fim'" class="urna-tela-fim">fim da votação</div>

  </div>
 
</template>

<script>
export default {
  name: "urna_tela",
  props: {
    tela: String,
  },
};
</script>

<style>
.urna-tela {
  width: 55%;
  height: 100%;
  background-color: var(--ballot-box-screen-color);
  border-radius: 5px;
  border: 2px solid var(--light-border-color);
  padding: 20px;
  color: var(--dark-text-color);
}
</style>