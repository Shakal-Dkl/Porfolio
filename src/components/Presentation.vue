<template>
  <main>
    <section class="home">
      <div class="home-content">
        <h1>Bonjour,<br />je m'appelle Ambroise Rony</h1>
        <h3>Developpeur Front-end</h3>
        <p>
          Je suis actuellement en formation Développeur Web et Web Mobile
          (DWWM), pour acquérir les compétences requises pour ma future
          carrière... Vous trouverez certains de mes projets en ici..., <br />de
          quoi prendre contact avec moi. il y aura des mise a jour,
          amélioration, nouveau contenu au fur et a mesure de mon avancer dans
          la formation et plus.
        </p>
      </div>
    </section>
    <section class="logo">
      <img src="./icons/pngegg.png" alt="logo" />
    </section>
  </main>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.home {
  height: 60vh;
  display: flex;
  align-items: center;
  padding: 0 10%;
}

.home-content {
  max-width: 800px;
}
.home-content h1 {
  font-size: 4rem;
  font-weight: 700;
  line-height: 1.2;
}
.home-content h3 {
  margin: 20px;
  font-size: 3rem;
  font-weight: 700;
  color: #00abf0;
}
.home-content p {
  font-size: 1.5rem;
}

.logo {
  display: flex;
  align-items: center;
  justify-content: center;
}
.logo img {
  width: 400px;
  height: 150px;
  border: #00abf0;
}
</style>
