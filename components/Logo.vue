<template>
  <div class="mx-auto logo" :class="dark ? 'dark' : ''">
    <span class="logo-icon text-left">
      <font-awesome-icon :icon="['far', 'list-alt']" />
    </span>
    <span class="absolute create uppercase">Create</span>
    <span class="absolute resume uppercase">Resume</span>
  </div>
</template>

<script>
export default {
  name: "Logo",
  props: {
    dark: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
.logo {
  width: 85px;
  padding: 0;
  position: relative;
  height: 30px;
}
.create,
.resume {
  font-size: 10px !important;
  font-weight: 800 !important;
  color: #c7ddea;
  letter-spacing: 2px;
  position: absolute;
  font-family: "Poppins", sans-serif !important;
}
.create {
  top: 3px;
  left: 35px;
}
.resume {
  top: 14px;
  left: 35px;
}
.logo-icon {
  position: absolute;
  left: 0;
}
.logo-icon svg {
  width: 30px !important;
  height: 30px !important;
  color: #c7ddea;
}

.dark.logo svg,
.dark.logo .resume,
.dark.logo .create {
  color: #125379;
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
