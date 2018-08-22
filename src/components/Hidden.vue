<template>
  <div id="hidden">
    <div class="flex-container">
      <h1>This is test component page accessible through the navbar</h1>
      <!-- <div class="flex-1"></div>
      <div class="flex-2">
        <router-link v-bind:to="'/'">Home</router-link>
        <router-link v-bind:to="'/about'">About</router-link>
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'hidden'
}
</script>
<!-- styling for the component -->
<style>
#hidden {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 5vw;
}
.flex-container{
  display: flex;
  height: 50vh;
  width: 100vw;
  background-color: mediumaquamarine;
  align-items: flex-start;

}
.flex-1{
  height: 100px;
  width: 50vw;
  background-color: bisque;
}
.flex-2{
  height: 200px;
  width: 50vw;
  background-color: brown;
}
</style>