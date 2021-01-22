<template>
  <div>
    <div class="slide-in-menu" ref="slideInMenu">
      <div>
        <ul>
          <li class="nav-item">
            <a href="" class="nav-link">Login</a>
          </li>
          <li class="nav-item">
            <a href="" class="nav-link">Login</a>
          </li>
          <li class="nav-item">
            <a href="" class="nav-link">Login</a>
          </li>
        </ul>
      </div>
      <button class="close-menu--btn btn" @click="slideOut">
        <font-awesome-icon :icon="['fas', 'chevron-circle-left']" />
      </button>
      <div class="overlay"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SlideInMenu",
  props: {},
  watch: {
    open: {
      handler(val) {
        this.slideIn();
      },
      deep: true,
    },
  },
  data() {
    return {
      showCloseMenuBtn: false,
      auth: false,
    };
  },
  methods: {
    slideIn() {
      console.log("clicked slide menyy");
      console.log(this.$refs);
      console.log(this.$refs.slideInMenu.classList);
      this.$refs.slideInMenu.classList.remove("slide-out");
      this.$refs.slideInMenu.classList.add("slide-in");
      const that = this;
      setTimeout(function () {
        that.showCloseMenuBtn = true;
      }, 300);
    },
    slideOut() {
      console.log("clicked slide menyy");
      console.log(this.$refs);
      console.log(this.$refs.slideInMenu.classList);
      this.$refs.slideInMenu.classList.remove("slide-in");
      this.$refs.slideInMenu.classList.add("slide-out");
      const that = this;
      setTimeout(function () {
        that.showCloseMenuBtn = false;
      }, 300);
    },
  },
};
</script>

<style scoped>
.slide-in-menu ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
.nav-link {
  padding: 5px 20px !important;
  font-size: 12px;
  font-weight: 700;
  color: white !important;
}
.slide-in-menu {
  background-color: rgb(31, 41, 55) !important;
  /*background: red;*/
  position: fixed;
  width: 80%;
  height: 100vh;
  top: 0;
  left: -2000px;
  bottom: 0;
  z-index: 100000000;
  padding: 20px 0;
}
.close-menu--btn {
  position: absolute;
  right: -70px;
  top: 40px;
  z-index: 1;
  color: white !important;
}
.close-menu--btn svg {
  width: 40px !important;
  height: 40px !important;
}
.overlay {
  background: #1f1d1d52;
  position: absolute;
  left: 100%;
  right: -30%;
  height: 100vh;
  top: 0;
}
.slide-in {
  -webkit-animation: menu-slide-right 0.5s forwards;
  animation: menu-slide-right 0.5s forwards;
}
.slide-out {
  -webkit-animation: menu-slide-left 0.5s forwards;
  animation: menu-slide-left 0.5s forwards;
}
@keyframes menu-slide-right {
  0% {
    z-index: 100000000;
    left: -2000px;
  }
  100% {
    left: 0%;
    width: 80%;
    z-index: 100000000;
  }
}
@-webkit-keyframes menu-slide-right {
  0% {
    z-index: 100000000;
    left: -2000px;
  }
  100% {
    left: 0%;
    width: 80%;
    z-index: 100000000;
  }
}
@keyframes menu-slide-left {
  0% {
    left: 0%;
    width: 80%;
    z-index: 100000000;
  }
  100% {
    left: -2000px;
    width: 80%;
    z-index: 100000000;
  }
}
@-webkit-keyframes menu-slide-left {
  0% {
    left: 0%;
    width: 80%;
    z-index: 100000000;
  }
  100% {
    left: -2000px;
    width: 80%;
    z-index: 100000000;
  }
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
}

/* Large Mobile :480px. */

@media only screen and (min-width: 480px) and (max-width: 575px) {
}

@media only screen and (max-width: 575px) and (min-width: 480px) {
}
</style>
