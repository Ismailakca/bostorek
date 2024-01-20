<template lang="">
  <div class="container">
    <SectionHeader title="Books" text="Books Text" />
    <BookList :books="paginatedBooks" />
    <Pagination :currentPage="currentPage" :totalPages="totalPages" />
  </div>
</template>
<script>
import SectionHeader from "@/components/SectionHeader.vue";
import BookList from "@/components/BookList.vue";
import Pagination from "@/components/Pagination.vue";
import books from "@/db.js";
export default {
  name: "BooksView",
  data() {
    return {
      books: books,
      currentPage: 1,
      itemsPerPage: 4,
    };
  },
  components: {
    SectionHeader,
    BookList,
    Pagination,
  },
  computed: {
    totalPages() {
      return Math.ceil(this.books.length / this.itemsPerPage);
    },
    paginatedBooks() {
      const startIndex = (this.currentPage - 1) * this.itemsPerPage;
      const endIndex = startIndex + this.itemsPerPage;
      return this.books.slice(startIndex, endIndex);
    },
  },
};
</script>
<style scoped>
.auth-box {
  margin-top: -30px;
}
</style>
