<template>
  <section class="products">
    <ul class="products__list">
      <li class="products__item"
        v-for="productItem in productsList"
        :key="productItem.productId"
      >
        <Card :productItem="productItem"></Card>
      </li>
    </ul>
  </section>
</template>

<script>
import Card from './Product/Card.vue';
import ProductsData from "../../db/products.json";

export default {
  name: "Products",
  components: {
    Card
  },
  data () {
    return {
      productsList: ProductsData,
    }
  }
};
</script>

<style>

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
    height: 305px;
  }
}

</style>
