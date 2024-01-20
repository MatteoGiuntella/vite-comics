<script>
export default {
    data() {
        return {

        };
}}
</script>

<template>
    <main>
       <div class="container-bg-main-top">
            <div class="container-general">
                
            </div>
       </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins.scss' as *;

main{
    .container-bg-main-top{
        width: 100%;
        background-color: black;
        .container-general{
            @include containerGeneralNoFlex;
            h1{
                color: white;
            }
        }
    }
}
</style>
<!-- Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass! -->