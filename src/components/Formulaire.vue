<template>
  <section class="contact" id="contact">
    <h1 class="titre">Contactez Moi !</h1>
    <p class="status" v-if="status">{{ status }}</p>

    <form id="form" @submit.prevent="sendEmail" action="#">
      <div class="input-box">
        <div class="input-field">
          <input
            type="text"
            id="nom"
            v-model="form.nom"
            placeholder="Nom"
            required
          />
          <span class="focus"></span>
        </div>
        <div class="input-field">
          <input
            type="text"
            id="prenom"
            v-model="form.prenom"
            placeholder="Prenom"
            required
          />
          <span class="focus"></span>
        </div>
      </div>

      <div class="input-box">
        <div class="input-field">
          <input
            type="text"
            id="objet"
            v-model="form.objet"
            placeholder="Objet"
            required
          />
          <span class="focus"></span>
        </div>
        <div class="input-field">
          <input
            type="email"
            id="email"
            v-model="form.email"
            placeholder="Email"
            required
          />
          <span class="focus"></span>
        </div>
      </div>

      <div class="textarea-field">
        <textarea
          v-model="form.message"
          name=""
          id="message"
          cols="30"
          rows="10"
          placeholder="Votre Message"
          required
        ></textarea>
        <span class="focus"></span>
      </div>

      <div class="container_btn">
        <button type="submit" id="button" class="btn">Envoyer</button>
      </div>
    </form>
  </section>
</template>

<script>
import emailjs from "@emailjs/browser";

export default {
  data() {
    return {
      form: {
        nom: "",
        prenom: "",
        email: "",
        objet: "",
        message: "",
      },
      status: "",
    };
  },
  methods: {
    sendEmail() {
      if (!this.verifChamps()) {
        return (this.status = " veuillez remplir tous les champs");
      }
      const serviceID = "service_gflp98k";
      const templateID = "template_vux1erl";
      const userID = "vUJq0rUeLxzDZ-OLd";
      emailjs.send(serviceID, templateID, this.form, userID).then(
        (response) => {
          console.log("SUCCESS!", response.status, response.text);
          this.status = "Email envoyé avec succès !";
        },
        (error) => {
          console.log("FAILED...", error.status, error.text);
          this.status = "Erreur lors de votre envoi mail.";
        }
      );
      //appel de la methods (resetForm) apres la methods sendMail.
      this.resetForm();
    },
    //methods de verification des champs.
    verifChamps() {
      return this.form;
    },

    //methods qui reset le formulaire.
    resetForm() {
      this.form.nom = "";
      this.form.prenom = "";
      this.form.email = "";
      this.form.objet = "";
      this.form.message = "";
    },
  },
};
</script>

<style scoped>
.status {
  display: flex;
  justify-content: center;
  font-size: 1.5rem;
  font-weight: bold;
}
.titre {
  display: flex;
  justify-content: center;
  font-size: 5rem;
  padding-bottom: 50px;
}
.contact {
  padding-top: 100px;
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

.btn {
  width: 150px;
  height: 50px;
  background: #081b29;
  background-color: ;
  border-radius: 15px;
  border: #00abf0 solid;
  color: #00abf0;
  font-size: 15px;
  font-weight: bold;
  cursor: pointer;
  position: relative;
  z-index: 1;
  overflow: hidden;
}
.btn:hover {
  color: #081b29;
}
.btn::after {
  content: "";
  background-color: yellowgreen;
  position: absolute;
  z-index: -1;
  left: -15%;
  right: -15%;
  top: 0;
  bottom: 0;
  transform: skewX(-45deg) scale(0, 1);
  transition: all 0.5s;
}
.btn:hover::after {
  transform: skewX(-45deg) scale(1, 1);
}
.btn:active {
  transform: translate(2px);
  box-shadow: 0 5px 10px black;
  color: #081b29;
}
</style>
