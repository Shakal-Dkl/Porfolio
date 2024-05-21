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
      <div class="btn-box">
        <a href="#">Compétences</a>
        <a href="#">CV</a>
      </div>
    </section>
  </main>
</template>

<style scoped>
.home {
  height: 80vh;
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
  font-size: 3rem;
  font-weight: 700;
  color: #00abf0;
}
.home-content p {
  font-size: 1.5rem;
  margin: 100px 0 100px;
}
.home-content .btn-box {
  display: flex;
  justify-content: space-between;
  width: 345px;
  height: 50px;
}
.btn-box a {
  position: relative;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 150px;
  height: 100%;
  background: yellowgreen;
  border: 2px solid #00abf0;
  border-radius: 8px;
  font-size: 19px;
  color: #081b29;
  text-decoration: none;
  font-weight: 600;
  letter-spacing: 1px;
  z-index: 1;
  overflow: hidden;
}

.btn-box a:hover {
  color: #00abf0;
}

.btn-box a:nth-child(2) {
  background: transparent;
  color: #00abf0;
}
.btn-box a:nth-child(2):hover {
  color: #081b29;
}

.btn-box a:nth-child(2)::before {
  background: #00abf0;
}

.btn-box a::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  background: #081b29;
  z-index: -1;
  transition: 1s;
}
.btn-box a:hover::before {
  width: 100%;
}
</style>
