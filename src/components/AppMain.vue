<script>
export default {
    data() {
        return {
            carditem:[
                {
                    image: '../../public/img/buy-comics-digital-comics.png',
                    title : 'Digital Comics',
                },
                {
                    image: '../../public/img/buy-comics-merchandise.png',
                    title : 'DC Merchandaise',
                },
                {
                    image: '../../public/img/buy-comics-shop-locator.png',
                    title : 'Comic shop locator',
                },
                {
                    image: '../../public/img/buy-comics-subscriptions.png',
                    title : 'Subcriptions',
                },
                {
                    image: '../../public/img/buy-dc-power-visa.svg',
                    title : 'DC Power Visa',
                }
        ],
        list1:[
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
        ],
        list2:[
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
        ],
        list3:[
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
        ],
        list4:[
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
            'lorem ipsum',
        ],
        };
    },
    methods: {

    }
}
</script>

<template>
    <main>
       <div class="container-bg-main-top">
            <div class="container-general">
                <h1>
                    Qui ci va il content
                </h1>
            </div>
       </div>
       <div class="container-bg-main-center">
            <div class="container-general">
                <ul>
                    <li v-for="(elem,i) in carditem">
                        <div>
                            <img :src="elem.image" alt="">
                        </div>
                        <span>
                            {{ elem.title }}
                        </span>
                    </li>
                </ul>
            </div>
       </div>
       <div class="container-bg-bottom">
            <div class="container-general">
                <div class="container-list">
                    <div class="list">
                        <h5>
                             DC COMICS
                        </h5>
                        <ul>  
                            <li v-for="(elem, index) in list1"  class="list-main-footer">
                                {{ elem }}
                            </li>
                        </ul>
                        <h5>
                            SHOP
                        </h5>
                        <ul>
                            <li v-for="(elem, index) in list2"  class="list-main-footer">
                                {{ elem }}
                            </li>
                        </ul>
                    </div>
                    <div class="list">
                        <h5>
                            DC
                        </h5>
                        <ul>
                            <li v-for="(elem, index) in list3" class="list-main-footer">
                                {{ elem }}
                            </li>
                        </ul>
                    </div>
                    <div class="list">
                        <h5>
                            SITES
                        </h5>
                        <ul>
                            <li v-for="(elem, index) in list4" class="list-main-footer">
                                {{ elem }}
                            </li>
                        </ul>
                    </div>

                </div>
                <div class="container-bg-logo">
                    
                </div>
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
    .container-bg-main-center{
        width: 100%;
        background-color: #0282F9;
        .container-general{
            width: 70%;
            margin: auto;
            padding: 20px;
            ul{
                display: flex;
                
                li{
                    width: 100%;
                    height: 100%;
                    display: flex;
                    flex-wrap: nowrap;
                    align-items: center;
                    justify-content: space-between;
                div{
                    display: flex;
                    justify-content: flex-end;
                    img{
                        height: 50%;
                        width: 50%;
                    }
                }
                span{
                    color: white;
                    font-weight: bold;
                    padding-left: 10px;
                }}
            }
        }
    }
    .container-bg-bottom{
        height: 400px;
        background-image: url("../../public/img/footer-bg.jpg");
        width: 100%;
        .container-general{
            width: 70%;
            height: 100%;
            margin: auto;
            display: flex;
            justify-content: space-between;
            position: relative;
            .container-list{
                display: flex;
                width: 30%;
                color: white;          
            }            
            .container-bg-logo{
                height: 100%;
                width: 40%;
                background-image: url("../../public/img/dc-logo-bg.png");
                background-size: contain;
                background-repeat: no-repeat;
                background-position: center;
                img{
                    height: 150%;
                }
            }
        }
    }
}
</style>
<!-- Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass! -->