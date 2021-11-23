<template>
  <div class="initiative">
    <section class="container">
      <div class="main-content">
        <div class="content">
          <h1>Nossa iniciativa</h1>
          <span>Somos desenvolvedores que se dedicam a fazer projetos perfeitos e
            entregar valor para todos os seus clientes. Gostamos de ver clientes
            satisfeitos com projetos feitos com carinho, atenção e qualidade
            altíssima.</span>
        </div>
        <div class="image">
          <!-- "Man image": Quando a pessoa não tem ideia do que colocar no alt o.O -->
          <img :src="image" alt="Man image" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// Como eu queria me livrar desses ../../../ isso aí é do capeta kakakaka.
import Image from "../../../assets/images/man-bg.webp";

export default {
  name: "Initiative",
  data: function () {
    return {
      image: Image,
    };
  },
};
</script>
