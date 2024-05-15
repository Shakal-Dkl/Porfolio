<template>
  <footer>
    <!--dans le footer on mettera les liens des réseaux et la maj du site-->
    <div class="Réseaux">
      <a href="#"><i class="bx bxl-linkedin"></i></a>
      <a href="#"><i class="bx bxl-facebook"></i></a>
      <a href="https://github.com/Shakal-Dkl" target="_blank"
        ><i class="bx bxl-github"></i
      ></a>
    </div>
    <div class="para">
      <p>Dernière mise a jour le 14 Mai 2024</p>
    </div>
  </footer>
</template>

<script></script>

<style scoped>
.para {
  display: flex;
  justify-content: center;
}
.Réseaux {
  display: flex;
  justify-content: center;
  justify-content: space-around;
}
.Réseaux a {
  position: relative;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;
  background: transparent;
  border: 2px solid #00abf0;
  border-radius: 50%;
  font-size: 20px;
  color: #00abf0;
  text-decoration: none;
  z-index: 1;
  overflow: hidden;
}
.Réseaux a:hover {
  color: #081b29;
}
.Réseaux a::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  background: yellowgreen;
  z-index: -1;
  transition: 0.5s;
}
.Réseaux a:hover:before {
  width: 100%;
}
</style>
