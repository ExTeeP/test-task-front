<template>
  <div class="product">
    <header class="product__header">
      <span class="product__code">Код: 147268</span>
      <span class="product__status">Наличие</span>
      <div class="product__photo">
        <a href="#" class="product__link">
          <img src="@/assets/df126-52f2-11e5-b9a9-00259036a192_220x220_1.jpg">
        </a>
      </div>
    </header>

    <div class="product__body">
      <div class="product__inner">
        <h4 class="product__title">
          <a href="#" class="product__link"
            >Ламинат 31 кл Kronospan Kronofix Афцелия Малайская 2,47 м.кв. 7 мм</a
          >
        </h4>

        <Tags class="product__tags"></Tags>
      </div>

      <div class="product__price">
        <div class="product__discount">
          <span class="product__discount-text">По карте<br />клуба</span>
          <span class="product__discount-price">375,71 &#8381;</span>
          <!-- <span class="rouble__i black__i">
            <svg
              version="1.0"
              id="rouble__b"
              xmlns="http://www.w3.org/2000/svg"
              x="0"
              y="0"
              width="30px"
              height="22px"
              viewBox="0 0 50 50"
              enable-background="new 0 0 50 50"
              xml:space="preserve"
            >
              <use
                xmlns:xlink="http://www.w3.org/1999/xlink"
                xlink:href="#rouble_black"
              ></use>
            </svg>
          </span> -->
        </div>

        <div class="product__retail">
          <span class="product__retail-price">391,09 &#8381;</span>
          <!-- <span class="rouble__i black__i">
            <svg
              version="1.0"
              id="rouble__g"
              xmlns="http://www.w3.org/2000/svg"
              x="0"
              y="0"
              width="30px"
              height="22px"
              viewBox="0 0 50 50"
              enable-background="new 0 0 50 50"
              xml:space="preserve"
            >
              <use
                xmlns:xlink="http://www.w3.org/1999/xlink"
                xlink:href="#rouble_gray"
              ></use>
            </svg>
          </span> -->
        </div>

        <div class="product__price-points">
          <p class="product__points">Можно купить за 231,75 балла</p>
        </div>

        <Units class="product__units"></Units>
      </div>
    </div>

    <footer class="product__footer">
      <Tooltip></Tooltip>

      <div class="product__footer-wrapper">
        <Stepper class="product__stepper"></Stepper>

        <button class="product__button button" type="button">
          <span class="product__button-text">В корзину</span>
        </button>
      </div>
    </footer>
  </div>
</template>

<script>
import Tags from "./Tags.vue";
import Units from "./Units.vue";
import Tooltip from "./Tooltip.vue";
import Stepper from "./Stepper.vue";

export default {
  name: "Card",
  props: {},
  components: {
    Tags,
    Units,
    Tooltip,
    Stepper,
  },
};
</script>

<style>
.product {
  width: 240px;
  height: 545px;
  padding: 10px 9px 18px;
  padding-left: 247px;
  position: relative;
  border: 1px solid #e0e0e0;
}

@media (min-width: 768px) {
  .product {
    width: 100%;
    height: 180px;
  }
}

@media (min-width: 1250px) {
  .product {
    height: 305px;
  }
}

.product__header {
  display: flex;
  justify-content: space-between;
}

.product__code {
  font-size: 12px;
  color: #666;
}

.product__status {
  cursor: pointer;
  color: #093;
  border-bottom: 1px dotted #093;
  text-decoration: none;
}

.product__status:hover {
  border-bottom-color: transparent;
}

.product__photo {
  position: absolute;
  left: 40px;
}

.product__link {
  display: block;
  color: inherit;
  text-decoration: none;
}

.product__link:hover {
  text-decoration: underline;
}

.product__photo img {
  max-width: 160px;
  max-height: 160px;
  display: block;
}

.product__body {
  display: flex;
  padding-top: 8px;
  justify-content: space-between;
}

.product__inner {
  max-width: 505px;
}

.product__title {
  margin: 0;
  padding-right: 70px;
  display: block;
  font-size: 16px;
  line-height: 24px;
  font-weight: 700;
  color: #000;
}

.product__tags {
  padding-top: 13px;
}

.product__price {
  line-height: 18px;
}

.product__discount {
  text-align: right;
  margin-bottom: 6px;
}

.product__discount-text {
  font-weight: 400;
  font-size: 14px;
  display: inline-block;
  text-align: right;
  line-height: 17px;
  margin-right: 23px;
}

.product__discount-price {
  font-size: 25px;
  font-weight: 700;
  color: #000;
}

.product__retail {
  text-align: right;
  margin-bottom: 8px;
}

.product__retail-price {
  font-size: 25px;
  color: #a7a7a7;
}

.product__price-points {
  font-size: 12px;
  line-height: 17px;
  color: #999;
  margin-bottom: 3px;
}

.product__points {
  margin: 0;
}

.product__footer {
  padding-top: 65px;
}

.product__footer-wrapper {
  display: flex;
  justify-content: flex-end;
}

.product__stepper {
  margin-right: 6px;
}

.product__button {
  min-width: 148px;
  min-height: 40px;
  border: none;
  color: #fff;
  background-color: #f90;
  text-align: center;
  position: relative;
  padding: 0 0 0 15px;
  cursor: pointer;
}

.product__button::after {
  content: "";
  width: 20px;
  height: 20px;
  position: absolute;
  left: 10px;
  top: 50%;
  margin-top: -10px;
  background-image: url('../../assets/icon-card.svg');
}

.product__button-text {
  font-size: 14px;
  line-height: 40px;
  text-transform: uppercase;
}

</style>
