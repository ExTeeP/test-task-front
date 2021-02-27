<template>
  <div class="stepper">
    <transition name="slide-fade">
      <Tooltip v-if="toolipIsVisible"></Tooltip>
    </transition>
    <input class="stepper__input" type="number" min="1" max="150"
      v-model="value"
      @blur="defaultValue"
      @keypress.enter="defaultValue"
      @mouseover="showTooltip"
      @mouseleave="hideTooltip"
    >
    <div class="stepper__arrow-wrapper">
      <button class="stepper__arrow stepper__arrow--up" @click="increaseValue" type="button"></button>
      <button class="stepper__arrow stepper__arrow--down" @click="decreaseValue" type="button"></button>
    </div>
  </div>
</template>

<script>
import Tooltip from "./Tooltip.vue";

export default {
  name: "Stepper",
  props: {},
  components: {
    Tooltip,
  },
  data() {
    return {
      value: 1,
      toolipIsVisible: false,
    };
  },
  methods: {
    showTooltip() {
      this.toolipIsVisible = true;
    },
    hideTooltip() {
      this.toolipIsVisible = false;
    },
    increaseValue() {
      this.value++;
    },
    decreaseValue() {
      this.defaultValue()
      this.value--
    },
    defaultValue() {
      if (this.value <= 1 || this.value === '') this.value = 1;
    }
  }

}
</script>

<style>
.stepper {
  display: flex;
  position: relative;
}

.stepper__input {
  border: 1px solid #ccc;
  color: #333;
  font-size: 13px;
  line-height: 1.2;
  margin: 0;
  overflow: hidden;
  padding: 12px 0 10px;
  width: 42px;
  text-align: center;
  outline: none;
}

.stepper__arrow-wrapper {
  margin-left: -1px;
}

.stepper__arrow {
  cursor: pointer;
  display: block;
  height: 50%;
  width: 25px;
  border: 1px solid #ccc;
  background: url('../../assets/jquery.fs.stepper-arrows.png') no-repeat #fff;
  outline: none;
}
.stepper__arrow:hover {
  background-color: #666;
}

.stepper__arrow--up {
  background-position: -29px 0;
  border-bottom: none;
}

.stepper__arrow--down {
  background-position: -29px -20px;
}

.stepper__arrow--up:hover {
  background-position: -1px 0;
}

.stepper__arrow--down:hover {
  background-position: -1px -20px;
}

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

input[type=number] {
  -moz-appearance: textfield;
}

.slide-fade-enter-active {
  transition: all .3s ease;
}

.slide-fade-leave-active {
  transition: all .4s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}

.slide-fade-enter, .slide-fade-leave-to {
  transform: translateX(10px);
  opacity: 0;
}
</style>
