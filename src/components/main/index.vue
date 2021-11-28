<!-- Se você não consegue rir com os garranchos do meu código, então pode deixar que faço isso por você. 😂😂😂😂 -->
<template>
  <main>
    <Top class="animate" />
    <Initiative class="animate" />
    <Contact class="animate" />
  </main>
</template>

<script>
import Top from "./top/index.vue";
import Initiative from "./initiative/index.vue";
import Contact from "./contact/index.vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
  name: "Main",
  mounted() {
    const sections = gsap.utils.toArray(".animate");

    sections.forEach((section) => {
      const animate = gsap.fromTo(
        section,
        { autoAlpha: 0, y: 50 },
        { duration: 1, autoAlpha: 1, y: 0 }
      );
      ScrollTrigger.create({
        trigger: section,
        animation: animate,
        toggleActions: "play none none none",
        once: true,
      });
    });
  },
  components: {
    Top,
    Initiative,
    Contact,
  },
};
</script>
