<template>
  <section class="products">
    <ul class="products__list">
      <li class="products__item">
        <Card></Card>
      </li>
      <li class="products__item">
        <Card></Card>
      </li>
    </ul>
  </section>
</template>

<script>
import Card from './Product/Card.vue';

export default {
  name: "Products",
  props: {},
  components: {
    Card
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.products {}

.products__list {
  margin: 0 auto;
  padding: 0;
  list-style: none;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

@media (min-width: 768px) {
  .products__list {
    flex-direction: column;
  }
}

.products__item {
  width: 240px;
  height: 545px;
  margin: 10px auto 0;
}

@media (min-width: 768px) {
  .products__item {
    width: 100%;
    height: 180px;
    margin-right: 0;
    margin-left: 0;
  }
}

@media (min-width: 1250px) {
  .products__item {
    height: 240px;
  }
}

</style>
