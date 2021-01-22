<template>
  <div
    class="main"
    :style="{
      background:
        'linear-gradient(147deg, rgba(15, 85, 131, 0.2), rgba(0, 0, 0, .3)), url(' +
        appUrl +
        '/images/bg.png) no-repeat',
      backgroundSize: 'cover',
    }"
  >
    <lander />
  </div>
</template>

<script>
import Lander from "~/components/Home/Lander";
export default {
  components: { Lander },
  data() {
    return {
      appUrl: process.env.APP_URL,
    };
  },
};
</script>

<style>
div.main {
  /*background: linear-gradient(*/
  /*    147deg,*/
  /*    rgba(15, 85, 131, 0.2),*/
  /*    rgba(0, 0, 0, 0.3)*/
  /*  ),*/
  /*  url("https://create-resume.test/images/bg.png") no-repeat;*/
  /*background-size: cover;*/
}
/*.container {*/
/*  margin: 0 auto;*/
/*  min-height: 100vh;*/
/*  display: flex;*/
/*  justify-content: center;*/
/*  align-items: center;*/
/*  text-align: center;*/
/*}*/

/*.title {*/
/*  font-family:*/
/*    'Quicksand',*/
/*    'Source Sans Pro',*/
/*    -apple-system,*/
/*    BlinkMacSystemFont,*/
/*    'Segoe UI',*/
/*    Roboto,*/
/*    'Helvetica Neue',*/
/*    Arial,*/
/*    sans-serif;*/
/*  display: block;*/
/*  font-weight: 300;*/
/*  font-size: 100px;*/
/*  color: #35495e;*/
/*  letter-spacing: 1px;*/
/*}*/

/*.subtitle {*/
/*  font-weight: 300;*/
/*  font-size: 42px;*/
/*  color: #526488;*/
/*  word-spacing: 5px;*/
/*  padding-bottom: 15px;*/
/*}*/

/*.links {*/
/*  padding-top: 15px;*/
/*}*/
</style>
