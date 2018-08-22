<template>
  <div id="app">
  <router-link v-bind:to="'/'">Home</router-link>
  <router-link v-bind:to="'/about'">About</router-link>
  <router-link v-bind:to="'/hidden'">Hidden</router-link>
  <!-- the router outlet, where all matched components would ber viewed -->
  <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
}
</script>
<!-- styling for the component -->
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#links{
  color: #2c3e50;
}
.navbar {
  padding: 0px !important;
  transition: 1s;
  height: 0vh;
  position: fixed !important;
  z-index: 1000;
  width: 100%;
  background: #f8f7f6 !important;
}

.navbar ul {
  text-align: center;
  margin-left: auto !important;
  margin-right: 50px !important;
  opacity: 0;
  transition-delay: 0.2s;
  transition-duration: 0.2s;
}

.navbar ul li {
  font-size: 2vw;
  line-height: initial;
  text-align: right;
}
@media only screen and (max-width: 768px) {
  .navbar ul li {
    font-size: 4vw;
  }
}

.navbar-brand {
  color: #999;
  z-index: 1001;
  position: fixed;
  top: 10px;
  left: 10px;
}

.navbar-toggler {
  z-index: 1001;
  position: fixed;
  top: 10px;
  right: 10px;
}

.animated-icon1 {
  width: 30px;
  height: 20px;
  position: relative;
  margin: 0px;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: 0.5s ease-in-out;
  -moz-transition: 0.5s ease-in-out;
  -o-transition: 0.5s ease-in-out;
  transition: 0.5s ease-in-out;
  cursor: pointer;
}

.animated-icon1 span {
  display: block;
  position: absolute;
  height: 3px;
  width: 100%;
  border-radius: 9px;
  opacity: 1;
  left: 0;
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  transform: rotate(0deg);
  -webkit-transition: 0.25s ease-in-out;
  -moz-transition: 0.25s ease-in-out;
  -o-transition: 0.25s ease-in-out;
  transition: 0.25s ease-in-out;
}

.animated-icon1 span {
  background: #999;
}

.animated-icon1 span:nth-child(1) {
  top: 0px;
}

.animated-icon1 span:nth-child(2) {
  top: 10px;
}

.animated-icon1 span:nth-child(3) {
  top: 20px;
}

.animated-icon1.open span:nth-child(1) {
  top: 11px;
  -webkit-transform: rotate(135deg);
  -moz-transform: rotate(135deg);
  -o-transform: rotate(135deg);
  transform: rotate(135deg);
}

.animated-icon1.open span:nth-child(2) {
  opacity: 0;
  left: -60px;
}

.animated-icon1.open span:nth-child(3) {
  top: 11px;
  -webkit-transform: rotate(-135deg);
  -moz-transform: rotate(-135deg);
  -o-transform: rotate(-135deg);
  transform: rotate(-135deg);
}
</style>