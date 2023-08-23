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
    <div class="container py-4">
      <div class="row">
        <div class="col" v-for="comic in comicsList">
          <ComicsCard :imgSrc="comic.thumb" :comicsType="comic.type"></ComicsCard>
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
</style>
