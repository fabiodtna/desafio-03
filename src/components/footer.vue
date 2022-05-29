<template>
  <nav>
    <div id="nomeContatos">
      <p>
        <strong>Fale Conosco</strong><br /><br />
        loja.com@email.com<br />
        tel:21000121212<br />
      </p>
    </div>
    <div id="Sobre">
      <ul>
        <li>Sobre Loja.com</li>
        <li>Nossas lojas</li>
        <li>Atendimento</li>
        <li>Estado</li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Footer_vue",
};
</script>
<style scoped>
nav {
  min-width: 700px;
  max-width: 1400px;
  margin: auto;
  background-color: #222;
  height: 150px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
#nomeContatos {
  color: white;
  display: flex;
  align-items: center;
  text-align: center;
  width: 30%;
}
#Sobre {
  color: white;
  display: flex;

  justify-content: center;
  width: 30%;
}
</style>