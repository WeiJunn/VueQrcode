<template>
  <div id="app">
    <div class="box">
      <qr></qr>
    </div>
  </div>
</template>

<script>
import Qr from "./components/qr.vue";
export default {
  name: "app",
  components: { Qr },
};
</script>

<style>
html,
body,
#app {
  display: flex;
  padding: 0px;
  margin: 0px;
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  border: hidden;
  justify-content: center;
  align-items: center;
  background-image: linear-gradient(to top right, #005aa7, #fffde4);
}
.box {
  justify-content: center;
  align-items: center;
}
</style>
