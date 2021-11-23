<template>
  <div class="contact" id="contact">
    <section class="container">
      <div class="main-content">
        <div class="content">
          <h1>Mande um oi, ligamos para você!</h1>
          <span>Preencha seus dados para que a gente possa entrar em contato.</span>
        </div>
        <form class="contact">
            <div class="form-group" ref="form">
                <label>Nome Completo:</label>
                <input type="text" name="name" ref="name" placeholder="Ex: Michel Domingos da Silva">
            </div>
            <div class="form-group">
                <label>Whatsapp:</label>
                <input type="text" name="phone" ref="phone" placeholder="(99) 99999-9999" v-on:input="handleBlur">
            </div>
            <div class="form-group">
                <button type="submit" name="btnSubmit" id="btnSubmit" v-on:click="handleSubmit">Peça uma reunião</button>
            </div>
        </form>
        <div class="message" ref="msg"></div>
      </div>
    </section>
  </div>
</template>

<script>

export default {
  name: "Contact",
  methods: {
    handleBlur(e) {
      const r = e.target.value.replace(/\D/g, "").match(/(\d{0,2})(\d{0,5})(\d{0,4})/),
        one = `${!r[2] ? r[1] : `(${r[1]}) `}`,
        two = `${r[2]}${r[3] ? `-${r[3]}` : ""}`;
      e.target.value = one + two;
    },

    handleSubmit(e) {
      e.preventDefault();
      
      const changeBorder = (el) => {
        el.value === "" ? el.setAttribute('style', 'border-color: red') : el.setAttribute('style', '');
      }

      const sendMessage = (el, msg, erro) => {
        erro ? el.setAttribute('style', 'border-color: green') : el.setAttribute('style', 'border-color: red');
        el.innerHTML = msg;
        el.style.display = "block";
      }

      const name = this.$refs.name,
        phone = this.$refs.phone,
        msg = this.$refs.msg;

      if (name.value === "" || phone.value === "") {
        sendMessage(msg, "Um ou mais campos estão vazios", false)
        changeBorder(name);
        changeBorder(phone);

      } else if (phone.value.length < 15){
        sendMessage(msg, "Preencha o seu Whatsapp completo", false)
        phone.setAttribute('style', 'border-color: red');
        
      } else {
        sendMessage(msg, "Dados enviados com sucesso! Em breve entraremos em contato pelo Whatsapp", true)
        changeBorder(name);
        changeBorder(phone);
      }
    },
  },
};
</script>
