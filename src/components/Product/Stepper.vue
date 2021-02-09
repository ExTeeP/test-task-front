<template>
  <div class="stepper">
    <input class="stepper__input" type="text" value="1">
    <div class="stepper__arrow-wrapper">
      <button class="stepper__arrow stepper__arrow--up" type="button"></button>
      <button class="stepper__arrow stepper__arrow--down" type="button"></button>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.stepper {
  display: flex;
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
</style>
