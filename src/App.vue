<script setup>
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
        <a href="" class="barra"><img src="/public/cart.svg" alt=""></a>
        <a href="" class="barra"><img src="/public/heart.svg" alt=""></a>
        <a href=""><img src="/public/profile.svg" alt=""></a>
      </div>
    
  </header>
  <main>
    <section class="bio">
      <div class="eric">
        <span>Autor de Abril</span>
        <h2>Eric-Emanuel Schimitt</h2>
        <p>
          Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions, and in 2001 he received the title of Chevalier des Arts et des Lettres. His books have been translated into over 40 languages.
        </p>
        <button>Acessar página do livro</button>
      </div>
      <div class="livro">
        <img src="/public/Schmitt_Nocognia_3D_500pcx 1.png" alt="">
        <p>*within the stock limit</p>
      </div>
    </section>
    <section class="info">
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
    <section class="lancamentos">
      <h2>Lançamentos</h2>
      <div class="cima">
        <div>
          <img src="/public/Chain of Iron: Volume 2.png" alt="">
          <h3>Chain of Iron: Volume 2</h3>
          <p class="autor">Cassandra Clare</p>
            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>

          <input type="button" value="Comprar">
        </div>
        <div>
          <img src="/public/Chain of Thorns.png" alt="">
          <h3>Chain of Thorns</h3>
          <p class="autor">Cassandra Clare</p>

            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>

          <input type="button" value="Comprar">
        </div>
        <div>
          <img src="/public/City of Fallen Angels.png" alt="">
          <h3>City of Fallen Angels</h3>
          <p class="autor">Cassandra Clare</p>

            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>

          <input type="button" value="Comprar">
        </div>
        <div>
          <img src="/public/Nona the Ninth.png" alt="">
          <h3>Nona the Ninth</h3>
          <p class="autor">Cassandra Clare</p>

            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>
    
          <input type="button" value="Comprar">
        </div>
      </div>
      <div class="baixo">
        <div>
          <img src="/public/Harlem Shuffle.png" alt="">
          <h3>Harlem Shuffle</h3>
          <p class="autor">Colson Whitehead</p>
   
            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>
    
          <input type="button" value="Comprar">
        </div>
        <div>
          <img src="/public/Two Old Women.png" alt="">
          <h3>Two Old Women</h3>
          <p class="autor">Velma Wallis</p>
        
            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>
         
          <input type="button" value="Comprar">
        </div>
        <div>
          <img src="/public/Carrie Soto Is Back.png" alt="">
          <h3>Carrie Soto Is Back</h3>
          <p class="autor">Taylor Jenkins Reid</p>
        
            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>
     
          <input type="button" value="Comprar">
        </div>
        <div>
          <img src="/public/Book Lovers.png" alt="">
          <h3>Book Lovers</h3>
          <p class="autor">Emily Henry</p>
        
            <p class="preco">R$23.24</p>
            <span><img src="/public/like.png" alt=""></span>
          
          <input type="button" value="Comprar">
        </div>
      </div>
    </section>
  </main>
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
.elements{
  display: flex;
  padding-right: 70px;
}
.elements a {
  margin: 10px;
}
.elements a.barra {
  border-right: 1px solid #4CAF50;
  padding-right: 20px;
}

main{
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
  border-radius: 2px;
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
.bio .eric button{
  background-color: #27AE60;
  border: none;
  color: white;
  padding: 14px 25px;
  font-size: 1.1rem;
  margin-top: 2vw;
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
.lancamentos h2 {
  font-weight: bold;
  font-size: 2.5rem;
  margin-left: 5vw;
}
.lancamentos .cima {
  display: flex;
  justify-content: center;
}
.lancamentos .baixo {
  display: flex;
  justify-content: center;
}
.lancamentos .cima div {
  padding: 1.5vw;
}
.lancamentos .baixo div {
  padding: 1.5vw;
}
.lancamentos .cima h3 {
  font-weight: bold;
  font-size: 1.6rem;
}
.lancamentos .cima .autor {
  color: #4F4C57;
}
.lancamentos .cima .preco {
  font-weight: bold;
}
.lancamentos .cima span {
  margin-left: 30px;
}
.lancamentos .cima .input {
  background-color: #27AE60;
}
</style>
