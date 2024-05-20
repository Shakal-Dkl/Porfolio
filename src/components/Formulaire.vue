<template>
  <section class="contact" id="contact">
    <h1 class="titre">Contactez Moi !</h1>

    <form id="form" action="#">
      <div class="input-box">
        <div class="input-field">
          <input type="text" id="name" placeholder="Nom" required />
          <span class="focus"></span>
        </div>
        <div class="input-field">
          <input type="text" id="prenom" placeholder="Prenom" required />
          <span class="focus"></span>
        </div>
      </div>

      <div class="input-box">
        <div class="input-field">
          <input type="text" id="objet" placeholder="Objet" required />
          <span class="focus"></span>
        </div>
        <div class="input-field">
          <input type="text" id="email" placeholder="Email" required />
          <span class="focus"></span>
        </div>
      </div>

      <div id="message" class="textarea-field">
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

      <div class="btn-box_btns">
        <button @click="sendEmail()" type="submit" id="button" class="btn">
          Envoyer
        </button>
      </div>
    </form>
  </section>
</template>

<script>
import emailjs from "emailjs";

export default {
  data() {
    return {
      form: {
        name: "",
        email: "",
        objet: "",
        message: "",
      },
      status: "",
    };
  },
  methods: {
    sendEmail() {
      const serviceID = "service_gflp98k";
      const templateID = "template_vux1erl";
      const userID = "vUJq0rUeLxzDZ-OLd";
      emailjs.send(serviceID, templateID, this.form, userID).then(
        (response) => {
          console.log("SUCCESS!", response.status, response.text);
          this.status = "Email envoyé avec succès !";
        },
        (error) => {
          console.log("FAILED...", error);
          this.status = "Erreur lors de votre envoi mail.";
        }
      );
    },
  },
};
</script>

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

.btn-box_btns {
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
</style>
