<template>
  <div class="home">
    <div id="div-left">
        <div id="div-search">
          <input id="input-search" placeholder="Pesquisa" />
          <button id="button-search">Search</button>
        </div>
      
        <div id="categories" 
        style="background-image:
        url(https://www.lojasolar.com.br/custom/content/themes/lojassolar/imagens/SEO/eletronicos-1.jpg);
        background-size:cover;">
            <h5 id="C-text">electronics</h5>
        </div>
        <div id="categories"
        style="background-image:
        url(https://mamasuncut.com/wp-content/uploads/2020/08/1-1.jpg);
        background-size:cover;">
            <h3 id="C-text">jewelery</h3>
        </div>
        <div id="categories"
        style="background-image:
        url(https://www.onlineshoppingguru.net/wp-content/uploads/2018/04/1-1.jpg);
        background-size:cover;">
            <h3 id="C-text">men's clothing</h3>
        </div>
        <div id="categories"
        style="background-image:
        url(https://i.pinimg.com/originals/62/c6/83/62c683f897eaec128e4a58c9f6709790.jpg);
        background-size:cover;">
            <h3 id="C-text">women's clothing</h3>
        </div>
    </div>
    <Modalview v-if="dialogo" @modal="fecharmodal" :id="iditem"/>
    <div id="div-right">
     <div class="grid">
      <div v-for="dados in dados" :key="dados.id" @click="getitem(dados.id)" id="div-anun">
        <div id="div-img" >
            <img id="img" :src="dados.image"/>
        </div>
        <div id="div-detalhes">
          <a id="txt-detalhe">{{dados.title.substring(0,20)}}<br/>
           Por: <strong> R${{dados.price}}</strong></a>
        </div>
      </div>
    </div> 
    </div>
  </div>
</template>

<script>
  import Modalview from '../components/modal.vue' ;

  export default{
    name:"Home_view",
    data(){
      return{
        dados: [],
        img: "https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg",
        dialogo: false,
        iditem: null
      }
    },
    components:{
        Modalview  
    },
    methods:{
      
    async Feeddata(){
      const res = await fetch("https://fakestoreapi.com/products")
      const data = await res.json()
      this.dados = data;
    },

    getitem(id){
      this.dialogo = true
      this.iditem = id;
    },

    fecharmodal(){
      this.dialogo = false
    }

    },
    created(){
      this.Feeddata()
    }
  }

</script>

<style scoped>
.home {
  min-width: 650px;
  max-width: 1250px;
  margin:auto;
  display: flex;
}
#div-left{
  display: flex;
  margin: 10px;
  width: 25%;
  flex-direction: column;
  align-items: center;
}
#div-search{
  display: flex;
  align-content: center;
  justify-content: center;
  margin: 10px;
  width: 90%;
}
#input-search {
  display: flex;
  padding: 5px;
  width: 60%;
  margin-bottom: 10px;
}
#categories{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 80%;
  background-color: aqua;
  height: 100px;
  margin: 10px;
}
#C-text{
  color: #ffffff;
  background-color:#222;
  padding: 5px;
  border-radius: 10px;
}
#button-search{
	background:linear-gradient(to bottom, #2dabf9 5%, #0688fa 100%);
	background-color:#2dabf9;
	border-radius:3px;
	border:1px solid #0b0e07;
	display:inline-block;
	cursor:pointer;
	color:#ffffff;
	font-family:Arial;
	font-size:10px;
  height: 30px;
	text-decoration:none;
	text-shadow:0px 1px 0px #263666;
  margin-left: 3%;
}
#button-search:hover {
	background:linear-gradient(to bottom, #0688fa 5%, #2dabf9 100%);
	background-color:#0688fa;
}
#button-search:active {
	position:relative;
	top:1px;
}
#div-right{
  display: flex;
  margin: 10px;
  width: 75%;
  justify-content:space-between;
}
#div-anun {
  height: 250px;
  width: 200px;
  margin: 10px;
  background-color: #222;
  display: inline-block;
}
#div-img{
  display: flex;
  justify-content: flex-end;
}
img{
  height: 180px;
  width: 200px;
  background-size:cover;
}
#div-detalhes{
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  height: 70px;
}
#txt-detalhe{
  font-size: 16px;
  color: #fff;
  max-width: 25ch;
}

@media only screen and (max-device-width: 850px) {
  /* fazer layout para telas menores */
  #div-anun {
  height: 250px;
  width: 200px;
  margin: 10px;
  background-color: #222;
  display: inline-block;
  }
  img{
    height: 180px;
    width: 200px;
    background-size:cover;
  }
  #div-search{
    display: flex;
    display: inline-block;
  }
  #input-search {
  display: flex;
  padding: 5px;
  width: 100%;
  margin-bottom: 10px;
  }
  #button-search{
    width: 50%;
    margin-left: 30%;
  }
}
</style>