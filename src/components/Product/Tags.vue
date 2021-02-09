<template>
  <div class="product-tags">
    <p class="product-tags__description">Могут понадобиться:</p>

    <ul class="product-tags__list">
      <li class="product-tags__item">
        <a class="product-tags__link" href="#">подложка,</a>
      </li>
      <li class="product-tags__item">
        <a class="product-tags__link" href="#">плинтус натуральный,</a>
      </li>
      <li class="product-tags__item">
        <a class="product-tags__link" href="#">рулетка,</a>
      </li>
      <li class="product-tags__item">
        <a class="product-tags__link" href="#">набор для укладки ламината,</a>
      </li>
      <li class="product-tags__item">
        <a class="product-tags__link" href="#">ножовка по ламинату,</a>
      </li>
      <li class="product-tags__item">
        <a class="product-tags__link" href="#">гель для стыков ламината Clic Protect.</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Tags",
  props: {},
};
</script>

<style>

.product-tags {
}

.product-tags__description {
  margin: 0;
  display: inline-block;
  margin-right: 4px;
  font-size: 13px;
  line-height: 16px;
  color: #545454;
  font-weight: 700;
}

.product-tags__list {
  padding: 0;
  list-style: none;
  display: inline;
}

.product-tags__item {
  display: inline;
  margin-right: 4px;
}

.product-tags__link {
  font-size: 13px;
  line-height: 16px;
  color: #666;
  text-decoration: none;
}

.product-tags__link:hover {
  text-decoration: underline;
}
</style>
