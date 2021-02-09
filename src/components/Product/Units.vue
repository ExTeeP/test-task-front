<template>
  <div class="product-units">
    <div class="product-units__wrapper">
      <button class="product-units__item product-units__item--active" type="button">
        <span class="ng-binding">За м. кв.</span>
      </button>
      <button class="product-units__item" type="button">
        <span class="ng-binding">За упаковку</span>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Units",
  props: {},
}
</script>

<style>
.product-units {
  text-align: right;
}

.product-units__wrapper {

}

.product-units__item {
  padding: 2px 6px;
  margin-right: 5px;
  font-size: 13px;
  color: #707070;
  background-color: transparent;
  transition: .2s;
  border: none;
  cursor: pointer;
}

.product-units__item--active {
  background: #000;
  cursor: default;
  color: #fff;
}

.product-units__item span {
  border-bottom: 1px dotted #707070;
}

.product-units__item:hover span {
  border-bottom: 1px solid transparent;
}

.product-units__item--active span {
  border-bottom: 1px dotted transparent;
}
</style>
