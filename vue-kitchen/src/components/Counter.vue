<template>
    <div class="stepper horizontal">
        <img @click='decrement()' src="https://alikinvv.github.io/stepper/build/img/arrow.svg" class="arrow top" alt="" />
        <div class="box">
            <p class="numbers1">{{ count }}</p>
        </div>
        <img @click='increment()' src="https://alikinvv.github.io/stepper/build/img/arrow.svg" class="arrow bottom" alt="" />
    </div>
</template>

<script>
export default {
    name: 'Counter',
    props: {
        initCountValue: {
            type: Number,
            default: 0
        }
    },
    data() {
        return {
            count: this.initCountValue
        }
    },
    methods: {
        increment() {
            if(this.count < 255) {
                return this.count ++
            }
        },
        decrement() {
            if(this.count >= 1) {
                return this.count --
            }
        },
    }
}
</script>

<style scoped>
.stepper {
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-weight: bold;
  font-size: 80px;
  font-family: "Roboto", sans-serif;
  border-radius: 8px;
}

.stepper.horizontal {
  position: relative;
  text-align: center;
  width: 300px;
  height: 119px;
  background-color: #ff6f72;
}
.stepper.horizontal .arrow {
  width: 70px;
  opacity: 0.5;
  transition: all 0.2s ease-in-out;
  cursor: pointer;
  position: absolute;
}
.stepper.horizontal .arrow:hover {
  opacity: 1;
}
.stepper.horizontal .arrow.top {
  transform: translateY(-50%);
  top: 59px;
  left: -11px;
}
.stepper.horizontal .arrow.bottom {
  transform: rotate(180deg) translateY(-50%);
  top: -12px;
  right: -11px;
}
.stepper.horizontal .box {
  overflow: hidden;
  height: 92px;
  width: 150px;
  position: relative;
  margin: 0 20px;
}
.stepper.horizontal .box::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 20px;
  background: linear-gradient(
    to right,
    #ff6f72 0%,
    rgba(125, 185, 232, 0) 100%
  );
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr="#ff6f72", endColorstr="#007db9e8",GradientType=1 );
  z-index: 1;
}
.stepper.horizontal .box::after {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  width: 20px;
  background: linear-gradient(
    to right,
    #ff6f72 0%,
    rgba(125, 185, 232, 0) 100%
  );
  filter: progid:DXImageTransform.Microsoft.gradient( startColorstr="#ff6f72", endColorstr="#007db9e8",GradientType=1 );
  z-index: 1;
  transform: rotate(180deg);
}

.stepper.horizontal .box .numbers1 {
  position: absolute;
  left: 5px;
  bottom: -80px;
  display: flex;
  transform: translateX(0);
  display: inline-block;
  letter-spacing: 1px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  width: 140px;
}
</style>