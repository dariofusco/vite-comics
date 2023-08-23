<script>
import TheHeader from './components/TheHeader.vue';
import TheFooter from './components/TheFooter.vue';
import ComicsCard from './components/ComicsCard.vue';
import comicsList from './db/comics';

export default {
  components: {
    TheHeader,
    TheFooter,
    ComicsCard,
  },
  data() {
    return {
      comicsList,
    };
  },
};
</script>

<template>
  <TheHeader></TheHeader>
  <main>
    <div class="hero"></div>
    <div class="container text-center py-5">
      <span class="badge badge-primary">CURRENT SERIES</span>
      <div class="row">
        <div class="col" v-for="comic in comicsList">
          <ComicsCard :imgSrc="comic.thumb" :comicsType="comic.type"></ComicsCard>
        </div>
      </div>
      <button type="button" class="btn btn-primary">LOAD MORE</button>
    </div>
    <div class="bar">
      <div class="container">
        <div class="row align-items-center">
          <div class="col">
            <img src="./assets/img/buy-comics-digital-comics.png" alt="">
            <span>DIGITAL COMICS</span>
          </div>
          <div class="col">
            <img src="./assets/img/buy-comics-merchandise.png" alt="">
            <span>DC MERCHANDISE</span>
          </div>
          <div class="col">
            <img src="./assets/img/buy-comics-subscriptions.png" alt="">
            <span>SUBSCRIPTION</span>
          </div>
          <div class="col">
            <img src="./assets/img/buy-comics-shop-locator.png" alt="">
            <span>COMIC SHOP LOCATOR</span>
          </div>
          <div class="col">
            <img src="./assets/img/buy-dc-power-visa.svg" alt="">
            <span>DC POWER VISA</span>
          </div>
        </div>
      </div>
    </div>
  </main>
  <TheFooter></TheFooter>
</template>

<style>
main {
  background-color: #1c1c1c;
}

.btn {
  border-radius: 0;
}

.hero {
  background-image: url(./assets/img/jumbotron.jpg);
  height: 400px;
}

.badge {
  border: 1px solid #0076e5;
  border-radius: 0;
  background-color: #0076e5;
  font-size: 20px;
  position: absolute;
  top: 74%;
  left: 16%;
}

.bar {
  background-color: #0076e5;
  padding: 2rem;
  color: white;
}

.bar img {
  width: 20%;
}
</style>
