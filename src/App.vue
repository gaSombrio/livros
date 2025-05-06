<script setup>
import { ref } from 'vue';
const produtos = [
  {
    id: 1,
    titulo: 'Chain of Iron: Volume 2',
    resenha: 'Cassandra Clare',
    preco: 23.24,
    capa: 'https://cdn.kobo.com/book-images/6db37b19-2d7d-4e5b-a1d8-b006188c9db4/1200/1200/False/the-last-hours-chain-of-iron.jpg',
  },
  {
    id: 2,
    titulo: 'Chain of Thorns',
    resenha: 'Cassandra Clare',
    preco: 23.24,
    capa: 'https://cdn.kobo.com/book-images/4aa958d8-c1ed-4bf2-90ce-fef019f92a15/353/569/90/False/the-last-hours-chain-of-thorns.jpg',
  },
  {
    id: 3,
    titulo: 'City of Fallen Angels',
    resenha: 'Cassandra Clare',
    preco: 13.94,
    capa: 'https://m.media-amazon.com/images/I/815MzJpG6iL._AC_UF1000,1000_QL80_.jpg',
  },
  {
    id: 4,
    titulo: 'Nona the Ninth',
    resenha: 'Cassandra Clare',
    preco: 16.84,
    capa: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcThSjYxA73VNaIFSItXwUsuMHkRQo7f8PXGBg&s',
  },
  {
    id: 5,
    titulo: 'Harlem Shuffle',
    resenha: 'Colson Whitehead',
    preco: 26.92,
    capa: 'https://m.media-amazon.com/images/I/81ZPFCh0xML.jpg',
  },
  {
    id: 6,
    titulo: 'Two Old Women',
    resenha: 'Velma Wallis',
    preco: 13.95,
    capa: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQBXEMa4hM454G7Whh7PrDN8R_oYebpPdFl_Q&s',
  },
  {
    id: 7,
    titulo: 'Carrie Soto Is Back',
    resenha: 'Taylor Jenkins Reid',
    preco: 26.04,
    capa: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGJROWBwFV4AHVxK1H0NNVTiEBBlVbmnf2gg&s',
  },
  {
    id: 8,
    titulo: 'Book Lovers',
    resenha: 'Emily Henry',
    preco: 15.81,
    capa: 'https://m.media-amazon.com/images/I/71Xy4AL7jKL.jpg',
  }
];
const mostrarCarrinho = ref(false);
const produtoSelecionado = ref(null);

function abrirCarrinho(produto) {
  produtoSelecionado.value = produto;
  mostrarCarrinho.value = true;
}

function voltarParaLoja() {
  mostrarCarrinho.value = false;
}
const carrinho = [
  {
    id: 7,
    titulo: 'Carrie Soto Is Back',
    resenha: 'Taylor Jenkins Reid',
    preco: 26.04,
    capa: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQGJROWBwFV4AHVxK1H0NNVTiEBBlVbmnf2gg&s',
  },
  {
    id: 8,
    titulo: 'Book Lovers',
    resenha: 'Emily Henry',
    preco: 15.81,
    capa: 'https://m.media-amazon.com/images/I/71Xy4AL7jKL.jpg',
    quantidade: 1,
  }
];

function diminuir(qnt) {

}
</script>

<template>
  <header>
    <div class="logo">
      <span class="main">IFbooks</span>
      <span class="sub">Apreço à leitura</span>
    </div>
    <div class="search-box">
      <input type="text" placeholder="Pesquisar" />
      <i class="fas fa-search search-icon"></i>
    </div>

    <nav>
      <a href="#">Termos</a>
      <a href="#">Equipe</a>
      <a href="#">Envio</a>
      <a href="#">Devoluções</a>
    </nav>
    <div class="elements">
      <button class="barra" @click="abrirCarrinho(produto)"><img src="/public/cart.svg" alt=""></button>
      <button class="barra"><img src="/public/heart.svg" alt=""></button>
      <button><img src="/public/profile.svg" alt=""></button>
    </div>

  </header>
  <main>
    <section class="bio" v-if="!mostrarCarrinho">
      <div class="eric">
        <span>Autor de Abril</span>
        <h2>Eric-Emanuel Schimitt</h2>
        <p>
          Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he received
          the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.
        </p>
        <button>Acessar página do livro</button>
      </div>
      <div class="livro">
        <img src="/public/Schmitt_Nocognia_3D_500pcx 1.png" alt="">
        <p>*within the stock limit</p>
      </div>
    </section>
    <section class="info" v-if="!mostrarCarrinho">
      <div class="frete">
        <img src="/public/Truck.png" alt="">
        <p class="txt">Frete grátis pra SC</p>
      </div>
      <div class="recomendados">
        <img src="/public/Star.png" alt="">
        <p class="txt">Livros recomendados</p>
      </div>
      <div class="vendas">
        <img src="/public/Book open.png" alt="">
        <p class="txt">Mais vendidos</p>
      </div>
    </section>

    <section class="lancamentos" v-if="!mostrarCarrinho">
      <h2>Lançamentos</h2>

      <div class="lista-produtos">
        <div class="produto" v-for="produto in produtos" :key="produto.id">
          <img :src="produto.capa" alt="" width="70%">
          <h3>{{ produto.titulo }}</h3>
          <p>{{ produto.resenha }}</p>
          <p class="preco">R${{ produto.preco }}</p>
          <button @click="abrirCarrinho(produto)">Comprar </button>

        </div>
      </div>
    </section>



    <section class="carrinho" v-if="mostrarCarrinho">
      <h2>Carrinho</h2>
      <div class="classes">
        <h3>Título</h3>
        <h3 class="q">Quantidade</h3>
        <h3>Subtotal</h3>
      </div>

      <div class="compras" v-for="produto in carrinho" :key="produto.id">
        <div>
          <img :src="produto.capa" alt="" width="8%">
          <div>
            <h3>{{ produto.titulo }}</h3>
            <p>{{ produto.resenha }}</p>
            <p class="preco">R${{ produto.preco }}</p>
          </div>
        </div>

        <div>
          <button @click="">-</button>
          <strong>{{ produto.quantidade }}</strong>
          <button>+</button>
        </div>


      </div>

      <button class="Vloja" @click="voltarParaLoja">Voltar para a loja</button>
      <div class="compra">
        <div>
          <input class="cupom" type="text" placeholder="código do cupom"> <input class="inserircpm" type="button"
            value="Inserir Cupom">
        </div>

        <div class="final">
          <h3>Total da Compra</h3>
          <p class="linha">Produtos:</p>
          <p class="linha">Frete:Grátis</p>
          <p>Total: </p>
          <input type="button" value="Ir para o pagamento">
        </div>
      </div>

    </section>


  </main>
  <footer>
    <div class="pe">
      <div class="unha">
        <p>IFbooks</p>
        <img src="/public/Vector.svg" alt="">
        <img src="/public/Vector (1).svg" alt="">
        <img src="/public/Vector (2).svg" alt="">
      </div>
      <div class="ifbook">
        <p>Contato</p>
        <div class="redes">
          <img src="/public/Icon.svg" alt="">
          <p>+55 47 40045263</p>
        </div>
        <div class="redes">
          <img src="/public/Icon (1).svg" alt="">
          <p>8h às 23h - Seg a Sex</p>
        </div>
        <div class="redes">
          <img src="/public/Icon (2).svg" alt="">
          <p>contato@ifbooks.com</p>
        </div>
        <div class="img">
          <img src="/public/paipal 1.svg" alt="paypal">
          <img src="/public/MasterCard-Logo-1979 1.svg" alt="Master Card">
          <img src="/public/VISA-card-logo- 1.svg" alt="Visa">
        </div>
      </div>
    </div>
    <div class="theLast">
      <P>© Alguns direitos reservados. IFbooks 2025. </P>
    </div>
  </footer>
</template>

<style scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 12px 30px;
  background-color: #fff;
  border-bottom: 2px solid #4CAF50;
  font-family: Arial, Helvetica, sans-serif;
}

.logo {
  display: flex;
  padding-left: 70px;

}

.logo .main {
  font-weight: bold;
  font-size: 18px;
  color: #222;
  padding-right: 10px;
  margin-top: 4px;
}

.logo .sub {
  font-size: 13px;
  color: #4CAF50;
  border-left: 1px solid #4CAF50;
  padding-left: 10px;
  width: 30%;
}

.search-box {
  flex: 1;
  max-width: 400px;
  margin: 0 30px;
  position: relative;
}

.search-box input {
  width: 100%;
  padding: 10px 35px 10px 15px;
  border: none;
  border-radius: 4px;
  background-color: #f2f2f2;
  font-size: 14px;
  outline: none;
}

.search-icon {
  position: absolute;
  right: 10px;
  top: 50%;
  transform: translateY(-50%);
  color: #777;
  font-size: 14px;
}

nav {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-right: 4vw;
}

nav a {
  text-decoration: none;
  color: #666;
  font-size: 14px;
  margin: 0 2vw 0 0;
}

.elements {
  display: flex;
  padding-right: 70px;
}

.elements button {
  border: none;
  background-color: white;
  margin-left: 15px;
}

.elements .barra {
  border-right: 1px solid #4CAF50;
  padding-right: 20px;
}

main {
  font-family: Arial, Helvetica, sans-serif;
}

.bio {
  display: flex;
  padding: 4vw 10vw;
  border-bottom: 1px solid #27AE60;

}

.bio .eric {
  margin-top: 7vw;
  margin-left: 6vw;
}

.bio .eric span {
  color: #27AE60;
  border: 1px solid;
  border-color: #27AE60;
  border-radius: 4px;
  padding: 12px 8px;
}

.bio .eric h2 {
  font-weight: bold;
  font-size: 3rem;
  color: #382C2C;
  margin-top: 3vw;
}

.bio .eric p {
  color: #4D4C4C;
  width: 60%;
  font-size: 1.1rem;
}

.bio .eric button {
  background-color: #27AE60;
  border: none;
  color: white;
  padding: 14px 25px;
  font-size: 1.1rem;
  margin-top: 2vw;
  border-radius: 4px;
}

.bio .livro {
  margin-right: 6vw;

}

.bio .livro p {
  margin: 0 0 5vw 14vw;
  position: absolute;

}

.info {
  padding: 2vw 5vw 3vw 5vw;
  display: flex;
  justify-content: center;
  border-bottom: 1px solid #27AE60;
}

.info div {
  display: flex;
  color: #231F2D;
  padding: 10px 7vw;

}

.info .txt {
  font-weight: bold;
  font-size: 1rem;
  margin-left: 15px;
}

.info .recomendados {
  border-left: 2px solid #937DC2;
  border-right: 2px solid #937DC2;
}

.lancamentos {
  padding: 6vw 6vw;
}

.lancamentos img {
  border-radius: 5px;
  max-height: 19vw;
}

.lancamentos h2 {
  font-weight: bold;
  font-size: 2.5rem;
  margin-left: 8vw;
  padding-bottom: 2vw;
}

.lancamentos h3 {
  font-size: 1.6rem;
}

.lancamentos p {
  color: #4F4C57;
}

.lancamentos .preco {
  font-weight: bold;
  color: #382C2C;
  font-size: 1.3rem;
}

.lancamentos button {
  color: white;
  background-color: #27AE60;
  border: none;
  border-radius: 4px;
  padding: 1vw 5vw;
  font-weight: bold;
  font-size: 1.1rem;
  margin-bottom: 6vw;
}

.lista-produtos {
  display: flex;
  flex-wrap: wrap;
  margin-left: 8vw;
}

.produto {
  flex: 0 0 calc(25% - 16px);
  box-sizing: border-box;
  padding: 2px;
}

.carrinho {
  padding: 8vw;

}

.carrinho h2 {
  color: #27AE60;
  font-size: 4rem;
  margin-left: 2vw;
  margin-bottom: 8vw;
}

.carrinho .classes {
  display: flex;
  justify-content: space-between;
  border-bottom: 1px solid #27AE60;
}

.carrinho .classes h3 {
  margin: 0 3vw 1vw;
  font-size: 2rem;
}

.carrinho .classes .q {
  margin-left: 16vw;
}

.carrinho .Vloja {
  margin-top: 6vw;
  border: 2px solid #aaaaaa;
  background-color: white;
  padding: 20px 60px;
  border-radius: 5px;
  font-weight: bold;
  font-size: 1.2rem;
}

.carrinho .cupom {
  margin-top: 6vw;
  border: 2px solid #000000;
  background-color: white;
  padding: 20px 60px;
  border-radius: 5px;
  font-weight: bold;
  font-size: 1.2rem;
}

.carrinho .inserircpm {
  margin-top: 6vw;
  border: none;
  background-color: #27AE60;
  padding: 20px 60px;
  border-radius: 5px;
  font-weight: bold;
  font-size: 1.2rem;
  color: white;
  margin-left: 1vw;
}

.carrinho .compra {
  display: flex;
}

.carrinho .final {
  border: 2px solid black;
  margin-left: 28vw;
  margin-top: 6vw;
  padding: 1vw;
  border-radius: 5px;
}

.carrinho .final h3 {
  font-size: 1.6rem;
}

.carrinho .final .linha {
  border-bottom: 1px solid #000000;
  padding-right: 17vw;
  padding-bottom: 1vw;
}

.carrinho .final input {
  background-color: #27AE60;
  color: white;
  border: none;
  padding: 20px 40px;
  border-radius: 5px;
  font-size: 1.2rem;
  margin-left: 3vw;
}


footer {
  background-color: #27AE60;
  padding: 3vw 8vw 1vw;
  font-family: Arial, Helvetica, sans-serif;
}

.pe {
  display: flex;
  justify-content: space-between;
}

.pe .unha {
  color: white;
  font-size: 1.2vw;
}

.pe .unha img {
  padding: 0 13px 0 0;
}

/*lado direito*/
.ifbook p {
  color: rgba(255, 255, 255, 0.76);
  font-size: 1.1vw;
}

.ifbook img {
  color: white;
  font-size: 1.1vw;
  margin-right: 15px;
}

.ifbook .redes {
  display: flex;
  align-items: center;
  /* Alinha verticalmente */
}

.redes span {
  padding: 0 7px 0 0;
}

/*cartoes*/
.img {
  padding: 1vw 0;
}

.img img {
  padding: 0 0.5vw;
}

/*theLast*/


.theLast {
  border-top: 1px solid white;
  color: #ffffff9c;
  font-size: 1.2vw;
  display: flex;
  justify-content: center;

}
</style>
