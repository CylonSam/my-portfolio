<script lang="ts">
import { defineComponent, defineEmits } from "vue";

export default defineComponent({
  // type inference enabled
  data() {
    count: 0;
  },
  emits: {
    changePage(page: string) {
      return page.length > 0;
    },
  },
  methods: {
    goToPage(page: string) {
      this.$emit("changePage", page);
    },
  },
});
</script>
<template>
  <div class="sidebar flex flex-col items-center justify-between">
    <div class="sidebar-header flex flex-col items-center">
      <img
        class="rounded-full h-24 w-24"
        src="../assets/img/profile-pic.jpg"
        alt=""
      />

      <div class="profile-name">Samantha Silva</div>
    </div>

    <div class="app-menu flex flex-col items-center sidebar-main">
      <a
        href="#"
        @click="goToPage('about')"
        class="sidebar-main-item active link"
        >about</a
      >
      <a href="#" class="sidebar-main-item inactive">projects</a>
      <a href="#" class="sidebar-main-item inactive">contact</a>
    </div>

    <div class="sidebar-footer flex flex-col items-center">
      <div class="social-icons flex justify-between">
        <font-awesome-icon
          class="social-icon m-0.5"
          :icon="['fab', 'twitter-square']"
          size="2x"
        ></font-awesome-icon>
        <font-awesome-icon
          class="social-icon m-0.5"
          :icon="['fab', 'github-square']"
          size="2x"
        ></font-awesome-icon>
        <font-awesome-icon
          class="social-icon m-0.5"
          :icon="['fab', 'linkedin']"
          size="2x"
        ></font-awesome-icon>
      </div>

      <div class="copyright">
        <p>
          Made with
          <font-awesome-icon
            class="copyright-heart"
            :icon="['fas', 'heart']"
          ></font-awesome-icon>
          and Vue in Belém @ 2021
        </p>
      </div>
    </div>
  </div>
</template>
<style scoped>
body {
  margin: 0;
}
.sidebar {
  /* 212121 */
  background: #1e2022;
  width: 20%;
  height: 100vh;
  padding: 4% 0 2%;
}

.profile-name {
  color: #c9d6df;
  font-weight: 400;
  font-size: 1.2rem;
  margin-top: 0.7em;
  font-family: "Oswald", sans-serif;
  /* font-family: "Cormorant Garamond", serif; */
}

.active {
  color: #52616b;
}

.inactive {
  color: #c9d6df;
}

.inactive:hover {
  color: #52616b;
}

.sidebar-main-item {
  font-weight: 400;
  font-size: 1.2rem;
  font-family: "Oswald", sans-serif;
}

/* .sidebar-main-item:hover {
  font-size: 1.3rem;
  color: #498467;
} */

.sidebar-footer {
  width: 100%;
}

.social-icon {
  color: #c9d6df;
}

.copyright {
  margin-top: 1.5rem;
}

.copyright p {
  color: #c9d6df;
  font-size: 0.8rem;
  font-family: "Oswald", serif;
}

.copyright-heart {
  color: crimson;
}
</style>
