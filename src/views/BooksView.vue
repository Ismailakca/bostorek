<template lang="">
  <div class="container">
    <SectionHeader title="Books" text="Books Text" />
    <BookList :books="books" />
  </div>
</template>
<script>
import SectionHeader from "@/components/SectionHeader.vue";
import BookList from "@/components/BookList.vue";
import books from "@/db.js";
export default {
  name: "BooksView",
  data() {
    return {
      books: books,
    };
  },
  components: {
    SectionHeader,
    BookList,
  },
};
</script>
<style scoped>
.auth-box {
  margin-top: -30px;
}
</style>
