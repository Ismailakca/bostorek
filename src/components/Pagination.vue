<template>
  <nav aria-label="Page navigation example">
    <ul class="pagination justify-content-end">
      <li class="page-item" :class="{ disabled: currentPage === 1 }">
        <a
          class="page-link"
          @click="backToPage(currentPage - 1)"
          aria-label="Previous"
        >
          <span aria-hidden="true">&laquo;</span>
        </a>
      </li>
      <li class="page-item" v-for="page in totalPages" :key="page">
        <a
          class="page-link"
          :class="{ active: currentPage === page }"
          @click="goToPage(page)"
          >{{ page }}</a
        >
      </li>

      <li class="page-item" :class="{ disabled: currentPage === totalPages }">
        <a
          class="page-link"
          @click="goToPage(currentPage + 1)"
          aria-label="Next"
        >
          <span aria-hidden="true">&raquo;</span>
        </a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Pagination",
  emits: ["page-change"],
  props: {
    currentPage: {
      type: Number,
      required: true,
    },
    totalPages: {
      type: Number,
      required: true,
    },
  },
  methods: {
    goToPage(page) {
      this.$emit("page-change", page);
    },
    backToPage(page) {
      this.$emit("back-change-page", page);
    },
  },
};
</script>

<style lang="scss" scoped></style>
