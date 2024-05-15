<template>
  <section class="contact" id="contact">
    <h1 class="titre">Contactez Moi !</h1>

    <form action="#">
      <div class="input-box">
        <div class="input-field">
          <input type="text" placeholder="Nom" required />
          <span class="focus"></span>
        </div>
        <div class="input-field">
          <input type="text" placeholder="Prenom" required />
          <span class="focus"></span>
        </div>
      </div>

      <div class="input-box">
        <div class="input-field">
          <input type="text" placeholder="Objet" required />
          <span class="focus"></span>
        </div>
        <div class="input-field">
          <input type="text" placeholder="Email" required />
          <span class="focus"></span>
        </div>
      </div>

      <div class="textarea-field">
        <textarea
          name=""
          id=""
          cols="30"
          rows="10"
          placeholder="Votre Message"
          required
        ></textarea>
        <span class="focus"></span>
      </div>

      <div class="btn-box btns">
        <button type="submit" class="btn">Envoyer</button>
      </div>
    </form>
  </section>
</template>

<script></script>

<style scoped>
.titre {
  display: flex;
  justify-content: center;
  font-size: 5rem;
}
.contact {
  padding-top: 5rem;
}

.contact form {
  width: 50%;
  margin: auto;
  text-align: center;
}

.contact form .input-box {
  position: relative;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.contact form .input-box .input-field {
  position: relative;
  width: 49%;
  margin: 0.8rem 0;
}

.contact form .input-box .input-field input,
.contact form .textarea-field textarea {
  width: 100%;
  height: 100%;
  padding: 1rem;
  font-size: 1rem;
  color: #ededed;
  background: transparent;
  border-radius: 0.6rem;
  border: 0.2rem solid;
  border-color: #00abf0;
}

.contact form .input-box .input-field input::placeholder,
.contact form .textarea-field textarea::placeholder {
  color: #ededed;
}

.contact form .textarea-field {
  position: relative;
  margin: 0.8rem 0 2.7rem;
  display: flex;
}

.contact form .textarea-field textarea {
  resize: none;
}
</style>
