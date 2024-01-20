<template lang="">
  <div class="row">
    <div
      v-for="book in books"
      :key="book.id"
      class="col-sm-6 col-md-4 col-xl-3 mb-4"
    >
      <BookItem :book="book" />
    </div>
  </div>
</template>
<script>
import BookItem from "./BookItem.vue";
export default {
  name: "BookList",
  components: {
    BookItem,
  },
  props: {
    books: {
      type: Array,
      default: () => [],
    },
  },
};
</script>
<style lang=""></style>
