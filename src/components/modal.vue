<template>
  <div id="view_modal" class="text-center">
    <div id="modal">
      <v-dialog v-model="dialog" width="500">
        <div id="div_item">
          <img id="img" :src="dados.image" />
          <div id="div_itemp">
            <a id="txtname">{{ dados.title }}</a>
            <a id="titledesc">R$ {{ dados.price }}</a>
          </div>
          <button id="btnexit" @click="$emit('modal')">x</button>
        </div>
        <div id="div_descri">
          <a id="titledesc">Descrição</a>
          <a id="txt_desc">{{ dados.description.substring(0, 300) }}</a>
        </div>
        <div id="div_btn">
          <button id="btncarrinho">Carrinho</button>
          <button id="btnfavo">Favoritar</button>
        </div>
      </v-dialog>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modal_comp",
  data() {
    return {
      dados: [],
      dialog: false,
    };
  },
  props: {
    id: String,
  },
  methods: {
    async getitem() {
      const resp = await fetch(`https://fakestoreapi.com/products/${this.id}`);
      const data = await resp.json();
      this.dados = data;
      console.log(this.dados);
    },
  },
  beforeMount() {
    this.getitem();
  },
};
</script>

<style scoped>
#view_modal {
  display: flex;
  align-content: center;
}
#modal {
  min-width: 350px;
  background-color: black;
  height: 300px;
  position: fixed;
  margin-top: 5%;
  width: 35%;
  border-radius: 10px;
}
#div_item {
  display: flex;
}
#img {
  margin: 10px;
  width: 150px;
  height: 100px;
  background-size: cover;
}
#div_itemp {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
#div_descri {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 5px;
}
#titledesc {
  font-size: 18px;
  font-weight: bold;
  color: #fff;
}
#txtname {
  color: #fff;
}
#txt_desc {
  color: #fff;
  text-align: center;
  font-size: 14px;
}
#btnexit {
  position: absolute;
  right: 0;
  margin: 5px;
  border-radius: 10px;
}
#div_btn {
  display: flex;
  justify-content: space-around;
  margin-top: 10px;
}
#btncarrinho {
  box-shadow: inset 0px 1px 0px 0px #97c4fe;
  background: linear-gradient(to bottom, #3d94f6 5%, #1e62d0 100%);
  background-color: #3d94f6;
  border-radius: 6px;
  border: 1px solid #337fed;
  display: inline-block;
  cursor: pointer;
  color: #ffffff;
  font-family: Arial;
  font-size: 14px;
  font-weight: bold;
  padding: 4px 20px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #1570cd;
}
#btncarrinho:hover {
  background: linear-gradient(to bottom, #1e62d0 5%, #3d94f6 100%);
  background-color: #1e62d0;
}
#btncarrinho:active {
  position: relative;
  top: 1px;
}
#btnfavo {
  box-shadow: inset 0px 1px 0px 0px #fbafe3;
  background: linear-gradient(to bottom, #ff5bb0 5%, #de4295 100%);
  background-color: #ff5bb0;
  border-radius: 6px;
  border: 1px solid #ee1eb5;
  display: inline-block;
  cursor: pointer;
  color: #ffffff;
  font-family: Arial;
  font-size: 15px;
  font-weight: bold;
  padding: 4px 20px;
  text-decoration: none;
  text-shadow: 0px 1px 0px #a60259;
}
#btnfavo:hover {
  background: linear-gradient(to bottom, #de4295 5%, #ff5bb0 100%);
  background-color: #de4295;
}
#btnfavo:active {
  position: relative;
  top: 1px;
}
</style>