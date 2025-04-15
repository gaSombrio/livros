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
    <section>
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
      </div>
      <p>*within the stock limit</p>
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



</style>
