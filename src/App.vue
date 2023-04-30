<template>
  <div class="box">
    <MainContentVue/>
  </div>
</template>

<script>
import MainContentVue from './components/MainContent.vue'
export default {
  name: 'App',
  components: {
    MainContentVue,
  },
}
</script>

<style>
input {
    letter-spacing: 2px;
}

.round-corner {
  border-radius: 6px;
}
.vertical-center {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
.init-input {
  display: block;
  padding: 0;
  margin: 0;
  outline: none;
  border: none;
  background-color: transparent;
}

.box {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  background: linear-gradient(200deg,#FF6666,#FFCCCC) no-repeat;
}
</style>