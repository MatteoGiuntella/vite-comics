<script>
export default {
    data() {
        return {
            item: [
                'characters',
                'comics',
                'movies',
                'tv',
                'games',
                'collectibles',
                'videos',
                'fans',
                'news',
                'shop',
            ]
        };
    },
    methods: {
      
    }
}
</script>

<template>
    <header>
       <div class="container-bg">
            <div class="container-general">
                 <div class="containerLogo">
                    <div class="logo">
                        <img src="../../public/img/dc-logo.png" alt="">
                    </div>  
                </div>
                <nav class="navbarHeader">
                   <ul class="navbarItem">
                    <li  v-for="(elem, index) in item">
                        {{ elem }}
                    </li>
                   </ul>
                </nav>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    .container-bg{
        width: 100%;
        background-color: white;

        .container-general {
            height: 100px;
            width: 70%;
            display: flex;
            justify-content: flex-end;
            margin: auto;
            .containerLogo{
                width: 50%;
                height: 100%;
                .logo{
                    width: 50%;
                    height: 100%;
                }
            }
            .navbarHeader{
                width: 100%;
                height: 100%;
                .navbarItem{
                    display: flex;
                    justify-content: center;
                    justify-content: space-between;
                    align-items: center;
                    flex-wrap: nowrap;
                    height: 100%;
                    li{
                        font-weight: bold;
                        height: 100%;
                        line-height: 70px;
                        &:nth-child(2){
                            border-bottom: 1px solid blue;
                            color: blue;
                        }
                    }
                }
            }

        }
    }

}
</style>
<!-- Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass! -->