<template>
  <main class="container">
    <div class="column-right">
      <Products></Products>
    </div>
  </main>
</template>

<script>
import Products from "./components/Products.vue";

export default {
  name: "App",
  components: {
    Products,
  },
};
</script>

<style>

*,
:after,
:before {
  box-sizing: border-box;
}

body,
html {
  height: 100%;
}

body {
  min-width: 320px;
  min-height: 100%;
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 14px;
  line-height: 1.4;
  color: #222222;
  background: #ffffff;
}

.container {
  width: 100%;
  margin: 0 auto;
  padding: 0 20px;
}

@media (min-width: 768px) {
  .container {
    width: 768px;
    padding: 0 9px;
  }
}

@media (min-width: 1250px) {
  .container {
    width: 1250px;
    padding: 0 40px;
  }
}

.column-right {
  width: 100%;
  margin: 20px 0 14px;
  display: flex;
  flex-direction: column;
}

@media (min-width: 1000px) {
  .column-right {
    width:750px
  }
}

@media (min-width: 1250px) {
  .column-right {
    width: 1000px;
  }
}

</style>
