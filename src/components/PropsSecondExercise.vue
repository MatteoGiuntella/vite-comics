<script>
export default {
  data() {
    return {};
  },
  props: {
    fumetto: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="pitcure">
      <img :src="fumetto.thumb" alt="" />
    </div>
    <div class="title-pitcure">
      {{ fumetto.series }}
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/mixins.scss" as *;
.card {
  height: 100px;
  width: calc(100% / 6);
  .pitcure {
    height: 200px;
    width: 150px;
    img {
      height: 100%;
      width: 100%;
    }
  }
  .title-pitcure {
    font-weight: bold;
    color: white;
    padding: 5px;
  }
}
</style>
<!-- Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass! -->
