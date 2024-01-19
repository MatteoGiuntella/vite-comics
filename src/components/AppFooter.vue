<script>
export default {
    data() {
        return {

        };
    },
    methods: {

    }
}
</script>

<template>
    <footer>
        
        <div class="container-bg-footer">
            <div class="container-footer">
                <div>
                    <button>
                        SIGN-UP NOW
                    </button>
                </div>
                <div class="container-item">
                    <h3>
                        FOLLOWAGE
                    </h3>
                    <span class="icon-footer"><img src="../../public/img/footer-facebook.png" alt=""></span>
                    <span class="icon-footer"><img src="../../public/img/footer-periscope.png" alt=""></span>
                    <span class="icon-footer"><img src="../../public/img/footer-pinterest.png" alt=""></span>
                    <span class="icon-footer"><img src="../../public/img/footer-twitter.png" alt=""></span>
                    <span class="icon-footer"><img src="../../public/img/footer-youtube.png" alt=""></span>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins.scss' as *;
footer{
    .container-bg-footer{
        @include footerContainer;
        .container-footer{
            margin: auto;
            width: 70%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding-top: 30px;
            div{
                button{
                border: 3px solid #0281F7;
                padding: 10px;
                color: white;
                background-color:  #303030;
                }
            }
            .container-item{
                display: flex;
                padding-left: 5px;
                justify-content: center;
                min-width: 50px;
                h3{
                color: #0281F7;
            }
            .icon-footer{
                height: 20px;
                width: 20px;
                margin-left: 5px;
                img{
                    width: 100%;
                    height: 100%;
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