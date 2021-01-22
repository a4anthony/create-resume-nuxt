<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <div class="container">
        <b-navbar-toggle target="navbar-toggle-collapse" @click="toggleSlideIn">
          <template #default="{ expanded }">
            <font-awesome-icon
              v-if="expanded"
              :icon="['fas', 'chevron-circle-down']"
            />
            <font-awesome-icon v-else :icon="['fas', 'chevron-circle-right']" />
          </template>
        </b-navbar-toggle>
        <b-navbar-brand href="#"><logo /></b-navbar-brand>

        <b-navbar-nav class="ml-auto d-none d-lg-flex">
          <b-nav-item v-if="!auth" href="#">Login</b-nav-item>
          <b-nav-item v-if="!auth" href="#">Register</b-nav-item>
          <!-- Navbar dropdowns -->
          <b-nav-item-dropdown v-if="auth" text="User" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </div>
    </b-navbar>
    <slide-in-menu ref="slideInMenu" />
  </div>
</template>

<script>
import Logo from "~/components/Logo";
import SlideInMenu from "@/components/Layout/SlideInMenu";
export default {
  name: "NavBar",
  computed: {
    auth() {
      return this.$store.state.auth.user;
    },
  },
  components: { SlideInMenu, Logo },
  data() {
    return {
      openMenu: false,
    };
  },
  methods: {
    toggleSlideIn() {
      console.log("clicked");
      this.$refs.slideInMenu.slideIn();
      this.openMenu = true;
    },
  },
};
</script>

<style scoped>
.navbar {
  background-color: rgb(31, 41, 55) !important;
}
.nav-link {
  padding: 5px 20px !important;
  font-size: 12px;
  font-weight: 700;
  color: white !important;
}
.nav-link:hover {
  background: rgba(55, 65, 81, 1);
  border-radius: 10px;
}
.navbar-brand {
  margin-right: auto !important;
  margin-left: 15px;
}

/* (1366x768) WXGA Display */

@media screen and (min-width: 1366px) and (max-width: 1919px) {
}

@media (min-width: 1198px) and (max-width: 1365.9px) {
}

/* Normal desktop :992px. */

@media (min-width: 992px) and (max-width: 1197px) {
}

/* Normal desktop :991px. */

@media (min-width: 768px) and (max-width: 991px) {
}

/* small mobile :576px. */

@media (min-width: 576px) and (max-width: 767px) {
}

/* extra small mobile 320px. */

@media (max-width: 575px) {
  /*#navbar-toggle-collapse {*/
  /*  padding: 20px 0;*/
  /*  border-top: 2px solid red;*/
  /*  position: absolute !important;*/
  /*  background-color: rgb(31, 41, 55) !important;*/
  /*  right: 0;*/
  /*  left: 0;*/
  /*  top: 53px !important;*/
  /*}*/
}

/* Large Mobile :480px. */

@media only screen and (min-width: 480px) and (max-width: 575px) {
}

@media only screen and (max-width: 575px) and (min-width: 480px) {
}
</style>
