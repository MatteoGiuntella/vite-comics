<script>
import secondoesercizio from "./PropsSecondExercise.vue";
export default {
  data() {
    return {
      carditem: [
        {
          image: "../../public/img/buy-comics-digital-comics.png",
          title: "Digital Comics",
        },
        {
          image: "../../public/img/buy-comics-merchandise.png",
          title: "DC Merchandaise",
        },
        {
          image: "../../public/img/buy-comics-shop-locator.png",
          title: "Comic shop locator",
        },
        {
          image: "../../public/img/buy-comics-subscriptions.png",
          title: "Subcriptions",
        },
        {
          image: "../../public/img/buy-dc-power-visa.svg",
          title: "DC Power Visa",
        },
      ],
      list1: [
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
      ],
      list2: ["lorem ipsum", "lorem ipsum", "lorem ipsum"],
      list3: [
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
      ],
      list4: [
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
        "lorem ipsum",
      ],
      book: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
  methods: {},
  components: {
    secondoesercizio,
  },
};
</script>

<template>
  <main>
    <div class="container-main-top-card">
      <div class="container-general" id="bg-top">
        <button class="button-blu" id="carrer">Current Series</button>
      </div>
    </div>
    <div class="container-bg-main-top">
      <div class="container-general-1">
        <secondoesercizio v-for="(elem, i) in book" :key="i" :fumetto="elem" />
        <div>
        <button class="button-blu">Load More</button>
      </div>
      </div>
      
    </div>
    <div class="container-bg-main-center">
      <div class="container-general">
        <ul>
          <li v-for="(elem, i) in carditem">
            <div>
              <img :src="elem.image" alt="" />
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
            <h5>DC COMICS</h5>
            <ul>
              <li v-for="(elem, index) in list1" class="list-main-footer">
                {{ elem }}
              </li>
            </ul>
            <h5>SHOP</h5>
            <ul>
              <li v-for="(elem, index) in list2" class="list-main-footer">
                {{ elem }}
              </li>
            </ul>
          </div>
          <div class="list">
            <h5>DC</h5>
            <ul>
              <li v-for="(elem, index) in list3" class="list-main-footer">
                {{ elem }}
              </li>
            </ul>
          </div>
          <div class="list">
            <h5>SITES</h5>
            <ul>
              <li v-for="(elem, index) in list4" class="list-main-footer">
                {{ elem }}
              </li>
            </ul>
          </div>
        </div>
        <div class="container-bg-logo"></div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../assets/scss/partials/mixins.scss" as *;

main {
  .container-main-top-card {
    width: 100%;
    min-height: 300px;
    background-image: url("../../public/img/jumbotron.jpg");
    background-size: cover;
    background-position: top;
    background-repeat: no-repeat;
    .container-general {
      @include containerGeneralNoFlex;
      position: relative;
      .button-blu {
        @include buttonblu;

        &#carrer {
          position: absolute;
          bottom: -220px;
        }
      }
    }
  }
  .container-bg-main-top {
    width: 100%;
    background-color: black;
    height: 700px;
    .container-general-1 {
      height: 100%;
      width: 70%;
      margin: auto;
      display: flex;
      flex-wrap: wrap;
      padding: 30px;
      position: relative;
      .button-blu{
        @include buttonblu;
        position: absolute;
        bottom: 5%;
        left: 50%;
        transform: translate(-50%);
      }
    }
  }
  .container-bg-main-center {
    width: 100%;
    background-color: #0282f9;
    .container-general {
      width: 70%;
      margin: auto;
      padding: 20px;
      ul {
        display: flex;

        li {
          width: 100%;
          height: 100%;
          display: flex;
          flex-wrap: nowrap;
          align-items: center;
          justify-content: space-between;
          div {
            display: flex;
            justify-content: flex-end;
            img {
              height: 50%;
              width: 50%;
            }
          }
          span {
            color: white;
            font-weight: bold;
            padding-left: 10px;
          }
        }
      }
    }
  }
  .container-bg-bottom {
    height: 400px;
    background-image: url("../../public/img/footer-bg.jpg");
    width: 100%;
    .container-general {
      width: 70%;
      height: 100%;
      margin: auto;
      display: flex;
      justify-content: space-between;
      position: relative;
      .container-list {
        display: flex;
        width: 30%;
        color: white;
      }
      .container-bg-logo {
        height: 100%;
        width: 40%;
        background-image: url("../../public/img/dc-logo-bg.png");
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        img {
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
