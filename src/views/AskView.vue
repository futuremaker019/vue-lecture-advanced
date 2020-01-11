<template>
  <div>
    <list-item></list-item>
    <!-- <ul class="news-list">
      <li v-for="item in fetchedAsk" class="post">
        <div class="points">{{ item.points }}</div>
        <div>
          <router-link v-bind:to="`item/${item.id}`">
            {{ item.title }}
          </router-link>

          <small class="link-text">
            {{ item.time_ago }}
            by
            <router-link 
            v-bind:to="`/user/${item.user}`" 
            class="link-text">
              {{ item.user }}
            </router-link>
          </small>
        </div>
      </li>
    </ul> -->
  </div>
</template>

<script>
// import { mapGetters } from "vuex";
import ListItem from '../components/ListItem.vue'

export default {
  // computed: {
  //   ...mapGetters(["fetchedAsk"])
  // },
  // created() {
  //   this.$store.dispatch("FETCH_ASK");
  // }
  components: {
    ListItem,
  }
};
</script>

<style scoped>

</style>
