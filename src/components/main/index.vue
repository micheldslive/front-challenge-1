<!-- Se você não consegue rir com os garranchos do meu código, então pode deixar que faço isso por você. 😂😂😂😂 -->
<template>
  <main>
    <Top />
    <Initiative />
    <Contact />
  </main>
</template>

<script>
import Top from "./top/index.vue";
import Initiative from "./initiative/index.vue";
import Contact from "./contact/index.vue";

export default {
  name: "Main",
  components: {
    Top,
    Initiative,
    Contact,
  },
};
</script>
