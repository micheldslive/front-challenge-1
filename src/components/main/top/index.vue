<template>
  <div class="top">
    <section>
      <div class="content">
        <span>Desenvolvedores prontos para ação</span>
        <h1>Seu projeto pronto na velocidade da luz</h1>
        <a href="#contact" rel="Button" v-on:click="handleClick">Peça uma reunião</a>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Top",
  methods: {
    handleClick(e) {
      const contact = document.getElementById("contact");
      contact.scrollIntoView();
      e.preventDefault();
    },
  },
};
</script>
