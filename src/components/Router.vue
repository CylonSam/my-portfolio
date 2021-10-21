<script lang="ts">
import { defineComponent } from "vue";

import Sidebar from "./Sidebar.vue";
import About from "./About.vue";

export default defineComponent({
  components: {
    Sidebar,
    About,
  },
  methods: {
    handlePageChange: (page: string) => {
      console.log("current page: " + page);
    },
  },
});
</script>
<template>
  <div class="flex">
    <Sidebar @changePage="handlePageChange($event)" />
    <About />
  </div>
</template>