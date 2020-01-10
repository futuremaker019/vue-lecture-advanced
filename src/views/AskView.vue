<template>
  <div>
    <p v-for="item in fetchedAsk">
      <!-- <a v-bind:href="item.url">{{ item.title }}</a> -->
      <router-link v-bind:to="`item/${item.id}`">
        {{ item.title }}
      </router-link>
      <small>{{ item.time_ago }} by {{ item.user }}</small>
    </p>
  </div>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  computed: {
    // #4 mapGetters의 배열화 선언 (getters의 함수명을 바로 사용가능하다.)
    ...mapGetters(["fetchedAsk"])

    // #3 mapGetters의 객체화 선언
    // ...mapGetters({
    //   fetchedAsk: 'fetchedAsk'
    // })

    // #2 mapState를 이용한 선언
    // ...mapState({
    //   ask: state => state.ask
    // }),

    // #1 기본 메서드 선언
    // ask() {
    //   return this.$store.state.ask;
    // }
  },
  created() {
    this.$store.dispatch("FETCH_ASK");
  }
};
</script>

<style></style>
