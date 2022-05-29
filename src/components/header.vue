<template>
  <nav>
    <div id="divtitulo">
      <img id="img" src="/img/logo.png" alt="" />
      <h2 id="title">Loja.com</h2>
    </div>
    <div id="rota">
      <router-link to="/">Home</router-link> |
      <router-link to="/compra">Carrinho</router-link>
    </div>
  </nav>
</template>


<script>
export default {
  name: "header_vue",
};
</script>
<style scoped>
nav {
  min-width: 600px;
  max-width: 1250px;
  margin: auto;
  background-color: #222;
  border-bottom: 4px solid #111;
  padding: 15px 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
#divtitulo {
  display: flex;
  align-items: center;
}
#img {
  width: 40px;
  height: 40px;
}
#title {
  margin-left: 10%;
  color: aliceblue;
}
nav a {
  font-weight: bold;
  color: aliceblue;
  font-size: 18px;
}

nav a.router-link-exact-active {
  color: #42b983;
}
#rota {
  margin-right: 0%;
  padding: 10px;
}
</style>