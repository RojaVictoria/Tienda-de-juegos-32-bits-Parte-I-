<template>
  <div id="app" class="text-center" >
    <img alt="Vue logo" src="./assets/logo.png">
    <Navbar></Navbar>
    <transition name="vista">
      <router-view></router-view>
    </transition>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
export default {
  components: { Navbar },
};
</script>

<style scoped>

.vista-enter-active, .vista-leave-active {
    transition: opacity .1s;
}
.vista-enter, .vista-leave-to{
    opacity: 0;
}
</style>
