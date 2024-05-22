<template>
  <div class="mainprojet">
    <section class="cv">
      <div class="left">
        <h2>Projet : CV</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem quasi,
          ex, distinctio libero doloremque labore quidem repellat iure quia
          atque mollitia. Saepe deserunt iure quod enim possimus repellat alias
          impedit!
        </p>
        <a href="https://github.com/Shakal-Dkl/Mon-CV.git" target="_blank"
          >Création d'un cv pour un devoir</a
        >
      </div>
      <div class="right">
        <a href="/img/Capture d’écran_22-5-2024_01139_.jpeg" target="_blank"
          ><img
            class="imgcv"
            src="/img/Capture d’écran_22-5-2024_01139_.jpeg"
            alt="img CV"
        /></a>
      </div>
    </section>

    <section class="cacharge">
      <div class="left">
        <h2>Projet : Cahier des chages</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto
          tenetur provident sequi sit dolore eius perspiciatis labore magni qui
          quam unde, veniam totam id. Minima molestias voluptas odit maiores ea.
        </p>
      </div>
      <div class="right">
        <a href="/img/Mon Cahier des Charges.pdf" target="_blank"
          ><img src="/img/CA.png" alt="img cahier des charges"
        /></a>
      </div>
    </section>

    <section class="dynaform">
      <div class="left">
        <h2>Projet : dynamiser un formulaire</h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolore
          aliquid ea nulla voluptate provident voluptatum architecto ipsam,
          maxime aliquam laboriosam quis ducimus id, ipsa non numquam! Esse quis
          veritatis distinctio?
        </p>
        <a
          class="link"
          href="https://github.com/Shakal-Dkl/DynamiserUnEspaceDeCommentaires_DocumentsDevoir.git"
          target="_blank"
        >
          Dynamiser un espace de eommentaires</a
        >
      </div>
      <div class="right">
        <a href="/img/Dyna.jpeg"
          ><img src="/img/Dyna.jpeg" alt="image dynamiser un formulaire"
        /></a>
      </div>
    </section>
  </div>
</template>

<script></script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.cv {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-top: 100px;
}
.cv h2 {
  text-align: center;
  font-size: 3rem;
}
.cv p {
  border: #00abf0 solid;
  background-color: yellowgreen;
  color: #081b29;
  padding: 10px;
  width: 400px;
  text-align: justify;
  margin: 100px;
  font-size: 30px;
}

.cv img {
  width: 300px;
  border: #00abf0 solid;
  box-shadow: 5px 5px 10px #00abf0;
}

.cacharge {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-top: 100px;
}
.cacharge h2 {
  text-align: center;
  font-size: 3rem;
}
.cacharge p {
  border: #00abf0 solid;
  background-color: yellowgreen;
  color: #081b29;
  padding: 10px;
  width: 400px;
  text-align: justify;
  margin: 100px;
  font-size: 30px;
}
.cacharge img {
  width: 300px;
  border: #00abf0 solid;
  box-shadow: 5px 5px 10px #00abf0;
}

.dynaform {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-top: 100px;
}
.dynaform h2 {
  text-align: center;
  font-size: 3rem;
}
.dynaform p {
  border: #00abf0 solid;
  background-color: yellowgreen;
  color: #081b29;
  width: 400px;
  text-align: justify;
  margin: 100px;
  font-size: 30px;
  padding: 10px;
}

.dynaform img {
  width: 300px;
  border: #00abf0 solid;
  box-shadow: 5px 5px 10px #00abf0;
}
.mainprojet a {
  text-decoration: none;
  color: #ededed;
  font-size: 20px;
}
.link:hover {
  background-color: yellowgreen;
  color: #081b29;
  border: yellowgreen solid;
  border-radius: 15px;
  transition: 0.9s;
}
</style>
