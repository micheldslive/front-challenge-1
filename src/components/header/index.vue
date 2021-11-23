<template>
  <header>
    <section>
      <div class="logo">
        <a href="/" rel="MeuFreela">
          {{ logo }}
        </a>
        </div>
      <div class="social">
        <a href="https://www.linkedin.com/in/micheldslive/" target="_blank" rel="Linkedin">
          <img :src="linkedin" alt="Linkedin" />
        </a>
        <a href="https://instagram.com/micheldslive/" target="_blank" rel="Instagram">
          <img :src="instagram" alt="Instagram" />
        </a>
        <a href="https://www.twitter.com/micheldslive/" target="_blank" rel="Twitter">
          <img :src="twitter" alt="Twitter" />
        </a>
      </div>
    </section>
  </header>
</template>

<script>
// Não siga meus imports, eu também to perdido. hahaha
import Linkedin from "../../assets/images/linkedin.webp";
import Instagram from "../../assets/images/instagram.webp";
import Twitter from "../../assets/images/twitter.webp";

export default {
  name: "Header",
  data: function () {
    return {
      linkedin: Linkedin,
      instagram: Instagram,
      twitter: Twitter,
    };
  },
  props: {
    logo: String,
  },
};
</script>
