<template>
  <header class="header">
    <h1 class="title">photophy</h1>
    <SearchPhoto v-on:search-photo="searchPhoto" />
  </header>
</template>

<script>
import SearchPhoto from '../SearchPhoto';

export default {
  name: "Header",
  components: {
    SearchPhoto
  },
  props: ["searchPhoto"]
}
</script>

<style scoped>
  .header {
    background: hsla(0,0,0,.5);
    color: #fff;
    display: inline-flex;
    font-size: 21px;
    justify-content: space-between;
    text-align: center;
    text-shadow: 14px orange;
    width: 100%;
  }

  .header a {
    color: #fff;
    padding-right: 5px;
  }

  .title {
    padding: 20px;
    letter-spacing: 1.7px;
    text-shadow: 3px 4px 5px rgba(243, 240, 240, 0.651);
  }

</style>
