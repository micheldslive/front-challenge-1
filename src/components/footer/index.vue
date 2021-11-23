<template>
  <footer>
    <section>
      <div>
        <p>Desafio 1 - front-end iniciante</p>
        <p>Iniciativa <a href="https://www.linkedin.com/in/mateusavilaisidoro/" target="_blank" rel="DevHall">
        {{ devHall }}</a></p>
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
    devHall: String,
  },
};
</script>
