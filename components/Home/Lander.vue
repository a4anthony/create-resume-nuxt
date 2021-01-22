<template>
  <div class="container no-padding-sm">
    <div class="row h-90-vh">
      <div class="col-lg-8 offset-lg-2 my-auto">
        <div class="lander text-center rounded my-auto">
          <div class="lander-logo">
            <logo dark />
          </div>
          <div class="lander-text text-center">
            <span>
              An online tool that helps you generate and download PDF formats of
              your resume by simply filling out a form.</span
            >
          </div>
          <div class="lander-btn text-center">
            <b-button class="create--btn"
              >Get Started
              <span class="ml-2">
                <font-awesome-icon :icon="['fas', 'chevron-right']" /> </span
            ></b-button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo";
export default {
  name: "Lander",
  components: { Logo },
};
</script>

<style scoped>
.create--btn {
  border: 2px solid #0f5583;
  color: #0f5583;
  background: transparent;
  font-weight: 700;
  font-size: 13px;
}
.create--btn:hover {
  color: white;
  background: #0f5583;
}
.lander {
  background: white;
  opacity: 0.95;
  padding: 40px 20px;
}
.lander-logo {
  height: 60px;
}
.lander-btn {
  margin-top: 30px;
}
.lander-text {
  font-weight: 700;
  font-size: 14px;
  width: 50%;
  margin: 0 auto;
  /*display: block;*/
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
  .lander-text {
    width: 100%;
  }
}

/* Large Mobile :480px. */

@media only screen and (min-width: 480px) and (max-width: 575px) {
}

@media only screen and (max-width: 575px) and (min-width: 480px) {
}
</style>
