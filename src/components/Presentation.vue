<template>
  <main>
    <section class="home">
      <div class="home-content">
        <h1>Bonjour,<br />je m'appelle Ambroise Rony</h1>
        <h3>Developpeur Front-end</h3>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ex sed
          temporibus laudantium autem ad quisquam corporis ducimus aperiam?
          Rerum, non reprehenderit odio laborum excepturi debitis voluptates?
          Ipsa dolorem possimus aliquid.
        </p>
      </div>
      <div class="btn-box">
        <a href="#">Compétences</a>
        <a href="#">Réalisations</a>
      </div>
    </section>
  </main>
</template>

<style scoped>
.home {
  height: 100vh;
  display: flex;
  align-items: center;
  padding: 0 10%;
}

.home-content {
  max-width: 500px;
}
.home-content h1 {
  font-size: 56px;
  font-weight: 700;
  line-height: 1.2;
}
.home-content h3 {
  font-size: 32px;
  font-weight: 700;
  color: #00abf0;
}
.home-content p {
  font-size: 16px;
  margin: 20px 0 40px;
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
  color: yellowgreen;
}

.btn-box a:nth-child(2) {
  background: transparent;
  color: yellowgreen;
}
.btn-box a:nth-child(2):hover {
  color: #081b29;
}

.btn-box a:nth-child(2)::before {
  background: yellowgreen;
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
