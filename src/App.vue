<template>
  <div id="app">
    <Navbar></Navbar>
    <div class="container">
      <h1>The clients names</h1>
      <Content></Content>
      <Pagination class="noprint"></Pagination>
    </div>
  </div>
</template>

<script>
import Content from "./components/Content.vue";
import Navbar from "./components/Navbar.vue";
import Pagination from "./components/Pagination.vue"


export default {
  name: "app",
  components: {
    Content,
    Navbar,
    Pagination
  }
};
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
}
.container{
  width:80%;
  padding: 10px;
  margin-top: 10px;
}
h1{
  text-align: center;
}
@media print{
  * {
    -webkit-print-color-adjust: exact !important;
  }
  .noBreak {
    break-inside: avoid;
  }
  .noprint {
    display: none;
  }
}
</style>
