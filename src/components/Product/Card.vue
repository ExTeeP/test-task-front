<template>
  <div class="product">
    <header class="product__header">
      <span class="product__code">Код: 147268</span>
      <span class="product_status">Наличие</span>
      <div class="product__photo">
        <a href="#" class="product__link">
          <img src="@/assets/df126-52f2-11e5-b9a9-00259036a192_220x220_1.jpg">
        </a>
      </div>
    </header>

    <div class="product__body">
      <h4 class="product__title">
        <a href="#" class="product__link"
          >Ламинат 31 кл Kronospan Kronofix Афцелия Малайская 2,47 м.кв. 7 мм</a
        >
      </h4>

      <Tags class="product__tags"></Tags>

      <Units class="product__units"></Units>

      <div class="product__price">
        <p class="product__price-discount">
          <span class="product__discount-text">По карте<br />клуба</span>
          <span class="product__discount-price">375,71</span>
          <span class="rouble__i black__i">
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
          </span>
        </p>

        <p class="product__price-retail">
          <span class="product__retail-price">391,09</span>
          <span class="rouble__i black__i">
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
          </span>
        </p>

        <div class="product__price-points">
          <p class="product__points">Можно купить за 231,75 балла</p>
        </div>
      </div>
    </div>

    <footer class="product__footer">
      <Tooltip></Tooltip>

      <div class="product__footer-wrapper">
        <Stepper class="product__stepper"></Stepper>

        <button
          class="product__button button"
          type="button"
          data-url="/cart/"
          data-product-id="9bf0afd7-5190-11e5-b9a9-00259036a192"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 512 512"
            width="20"
            height="20"
          >
            <path
              d="M508.764 74.466a14.77 14.77 0 00-11.533-5.542H104.152L93.16 21.294A14.77 14.77 0 0078.769 9.846h-64C6.613 9.846 0 16.459 0 24.616s6.613 14.769 14.769 14.769H67.02l74.612 323.321a14.77 14.77 0 0014.391 11.448h295.915c8.157 0 14.769-6.613 14.769-14.769 0-8.157-6.613-14.769-14.769-14.769H167.773l-11.36-49.231h296.511a14.769 14.769 0 0014.409-11.527L511.64 86.935a14.77 14.77 0 00-2.876-12.469zm-67.656 191.38H149.596L110.969 98.462h367.8l-37.661 167.384zM216.615 393.846c-29.86 0-54.154 24.293-54.154 54.154s24.293 54.154 54.154 54.154c29.86 0 54.154-24.293 54.154-54.154s-24.293-54.154-54.154-54.154zm0 78.77C203.042 472.616 192 461.573 192 448s11.042-24.615 24.615-24.615c13.573 0 24.615 11.042 24.615 24.615s-11.042 24.616-24.615 24.616zM393.846 393.846c-29.86 0-54.154 24.293-54.154 54.154s24.293 54.154 54.154 54.154c29.86 0 54.154-24.293 54.154-54.154s-24.293-54.154-54.154-54.154zm0 78.77c-13.573 0-24.615-11.042-24.615-24.615s11.042-24.615 24.615-24.615c13.573 0 24.615 11.042 24.615 24.615s-11.042 24.615-24.615 24.615z"
            />
          </svg>
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.product {
  width: 240px;
  height: 545px;
  padding: 10px 10px 18px;
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
    height: 240px;
  }
}

.product__code {
  font-size: 12px;
  color: #666;
}
</style>
