<template>
  <div id="Carrinho">
    <div id="produtos_div">

         <div id="items_div">   
        <img id="img" src="https://auctions.c.yimg.jp/images.auctions.yahoo.co.jp/image/dr000/auc0205/users/72a94bfbbf20f96ec37192b72d0ab1fab5b3f3f6/i-img400x400-1621418971odivfk759499.jpg"/>
        <div id="detalhep_div">
            <div>
              <p id="nome_item">Samsung 49-Inch CHG90 144Hz Curved Gaming Monitor (LC49HG90DMNXZA) – Super Ultrawide Screen QLED </p>
              <strong id="preco_item">$ 49,99</strong><br/>
              <a id="correio_item">Envio Gratuito através da Entrega Padrão (Correios)</a>
            </div>
          <div id="detalhec_div">
            <div><button>-</button><a id="txt_quant">1</a><button>+</button></div>
            <button id="btn_item" >favoritar</button>
            <button id="btn_item">excuir</button>
          </div>
        </div>
      </div>

       <div id="items_div">   
        <img id="img" src="https://auctions.c.yimg.jp/images.auctions.yahoo.co.jp/image/dr000/auc0205/users/72a94bfbbf20f96ec37192b72d0ab1fab5b3f3f6/i-img400x400-1621418971odivfk759499.jpg"/>
        <div id="detalhep_div">
            <div>
              <p id="nome_item">Blusa de frio luis vitao</p>
              <strong id="preco_item">$ 49,99</strong><br/>
              <a id="correio_item">Envio Gratuito através da Entrega Padrão (Correios)</a>
            </div>
          <div id="detalhec_div">
            <div><button>-</button><a id="txt_quant">1</a><button>+</button></div>
            <button id="btn_item" >favoritar</button>
            <button id="btn_item">excuir</button>
          </div>
        </div>
      </div>

       <div id="items_div">   
        <img id="img" src="https://auctions.c.yimg.jp/images.auctions.yahoo.co.jp/image/dr000/auc0205/users/72a94bfbbf20f96ec37192b72d0ab1fab5b3f3f6/i-img400x400-1621418971odivfk759499.jpg"/>
        <div id="detalhep_div">
            <div>
              <p id="nome_item">Blusa de frio luis vitao</p>
              <strong id="preco_item">$ 49,99</strong><br/>
              <a id="correio_item">Envio Gratuito através da Entrega Padrão (Correios)</a>
            </div>
          <div id="detalhec_div">
            <div><button>-</button><a id="txt_quant">1</a><button>+</button></div>
            <button id="btn_item" >favoritar</button>
            <button id="btn_item">excuir</button>
          </div>
        </div>
      </div>

       <div id="items_div">   
        <img id="img" src="https://auctions.c.yimg.jp/images.auctions.yahoo.co.jp/image/dr000/auc0205/users/72a94bfbbf20f96ec37192b72d0ab1fab5b3f3f6/i-img400x400-1621418971odivfk759499.jpg"/>
        <div id="detalhep_div">
            <div>
              <p id="nome_item">Blusa de frio luis vitao</p>
              <strong id="preco_item">$ 49,99</strong><br/>
              <a id="correio_item">Envio Gratuito através da Entrega Padrão (Correios)</a>
            </div>
          <div id="detalhec_div">
            <div><button>-</button><a id="txt_quant">1</a><button>+</button></div>
            <button id="btn_item" >favoritar</button>
            <button id="btn_item">excuir</button>
          </div>
        </div>
      </div>
        

      
    </div>
    

    <div id="resumo_div">
        <h3 id="txt_resumo">Resumo do Pedido</h3>
        <div id="div_precos">
          
          <div id="div_preco">
            <a id="txt_preco">Subtotal:</a>
            <a id="txt_preco">R$ 0,00</a>
          </div>
          
          <div id="div_preco">
            <a id="txt_preco">Frete:</a>
            <a id="txt_preco">R$ 0,00</a>
          </div>

          <div id="div_total">
              <div id="div_precoTotal">
                <a id="txt_total">Total</a>
                <a id="txt_total">R$ 0,00</a>
              </div>
              <button id="button_comprar">Comprar</button>
          </div>

        </div>
    </div>
    
  </div>
</template>

<script>
  export default{
    name:"Carrinho_view",

  }
</script>

<style scoped>
#Carrinho{
  min-width: 700px;
  max-width: 1250px;
  margin:auto;
  display: flex;
  flex-direction: row;
  justify-content: center;
}
#items_div{
  background-color:#222;
  display: flex;
  flex-direction: row;
  width: 95%;
  height: 125px;
  margin: 15px;
  align-items: center;
}
#produtos_div{
  width: 85%;
  margin: 5px;
}
#img{
  width: 100px;
  height: 100px;
  margin: 10px;
}
#detalhep_div{
  display: flex;
  flex-direction:row;
  justify-content: space-between;
  width: 90%;
  margin: 10px;
}
#detalhec_div{
  margin: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
#txt_quant{
  color: aliceblue;
  font-size: 16px;
  font-weight: bold;
}
#btn_item{
  width: 100%;
  margin-top: 5px;
}
button{
  margin: 3px;
}
#nome_item{
  font-size: 15px;
  font-weight: bold;
  color: aliceblue;
}
#preco_item{
  font-size: 17px;
  font-weight: bold;
  color: aliceblue;
}
#correio_item{
  font-size: 15px;
  color: aliceblue;
}


#resumo_div{
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #222;
  border-radius: 10px;
  width: 30%;
  height: 250px;
  margin: 10px;
  margin-bottom: 200px;
}
#div_precos{
  display: flex;
  flex-direction: column;
  background-color: aliceblue;
  margin: 5px;
  border-radius: 5px;
  width: 80%;
}
#div_preco{
  display: flex;
  justify-content:space-between;
  margin: 10px;
}
#div_total{
  display: flex;
  justify-content: center;
  flex-direction: column;
}
#div_precoTotal{
  display: flex;
  justify-content:space-between;
  margin: 5px;
}
#txt_resumo{
  color: #fff;
}
#txt_preco{
  font-size: 15px;
  font-weight: bold;
}
#txt_total{
  font-size: 18px;
  font-weight: bold;
}
#button_comprar{
  padding: 10px;
  background-color: rgba(42, 40, 154, 0.978);
  font-size: 16px;
  font-weight: bold;
}
</style>