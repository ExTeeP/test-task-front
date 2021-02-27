<template>
  <div class="product__tooltip">
    <div class="product__tooltip-inner">
      <span class="product__tooltip-text">Продается упаковками:</span>
      <span class="product__tooltip-count">1 упак. = 2.47 м. кв.</span>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.product__tooltip {
  position: absolute;
  width: 222px;
  right: -154px;
  bottom: 50px;
  padding: 5px 10px;
  padding-left: 40px;
  background: #fff;
  border: 1px solid #ccc;
}

.product__tooltip::before,
.product__tooltip::after {
  content: '';
  position: absolute;
  bottom: -7px;
  border-top: 8px solid;
  border-top-color: currentcolor;
  display: block;
  width: 0;
  height: 0;
}

.product__tooltip::after {
  border-color: #fff;
  border-right-color: rgb(255, 255, 255);
  border-left-color: rgb(255, 255, 255);
  left: 14px;
  border-left: 7px solid transparent;
  border-right: 7px solid transparent;
}

.product__tooltip::before {
  margin-bottom: -1px;
  border-color: #ccc;
  border-right-color: rgb(204, 204, 204);
  border-left-color: rgb(204, 204, 204);
  color: #ccc;
  left: 13px;
  border-left: 8px solid transparent;
  border-right: 8px solid transparent;
}

.product__tooltip-inner {
  display: flex;
  flex-direction: column;
}
.product__tooltip-inner::before {
  content: "";
  width: 15px;
  height: 15px;
  position: absolute;
  left: 10px;
  bottom: 14px;
  background-image: url('../../assets/unit--i.png');
  background-size: cover;
}

.product__tooltip-text,
.product__tooltip-count {
  font-size: 13px;
  line-height: 15px;
}
</style>
