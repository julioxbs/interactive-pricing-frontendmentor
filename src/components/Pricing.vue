<template>
  <div class="box-price rounded shadow">
      <div class="box-header p-3 text-center">
          <div class="price d-md-flex align-items-center justify-content-between">
              <p class="fw-bold text-muted views">100K PAGEVIEWS</p>
              <p class="text-muted"><span class="fw-bold">${{rangeValue}}.00</span> / month</p>
          </div>

          <div class="inputValue">
            <input v-model="rangeValue" type="range" class="w-100" min="0" max="32">
          </div>

          <div class="info d-flex align-items-center justify-content-center gap-3 text-muted mt-5">
              <p>Monthly Billing</p>

              <p @click="btnActive" class="activ" :class="monthBilling === true ? 'active-bg' : ''">
                  <span class="circle" :style="!monthBilling ? 'left: 4px;' : 'right: 4px;'"></span>
              </p>
              
              <p>Yearly Billing 
                  <span class="discont fw-bold rounded" style="font-size: 12px; padding: 1px 2px;">-25%</span>
              </p>
          </div>
      </div>

      <hr>

      <div class="box-foot p-3 text-center d-md-flex align-items-center justify-content-between">
          <ul class="p-0 m-0 d-flex flex-column gap-2">
              <li v-for="{name, id} in lists" :key="id" class="text-muted" style="font-size: 15px fw-bold">
                  <span><img src="/images/icon-check.svg" alt="icon"></span>
                  {{name}}
              </li>
          </ul>

          <a href="#" class="button fw-bold">Start my trial</a>
      </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            rangeValue: 16,
            monthBilling: false,

            lists: [
                {name: 'Unlimited websites', id: 1},
                {name: '100% data ownership', id: 2},
                {name: 'Email reports', id: 3},
            ]
        }
    },

    methods: {
        btnActive() {
            this.monthBilling = !this.monthBilling
        }
    }
}
</script>

<style scoped>
.box-price {
    width: 100%;
    max-width: 500px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -20%);
    background: #fff;
}

input[type=range]{
    -webkit-appearance: none;
}

input[type=range]::-moz-range-progress {
    background: var(--clr-StrongCyan);
}

input[type=range]::-webkit-slider-runnable-track {
    width: 100%;
    height: 10px;
    background: var(--clr-SoftCyan);
    border: none;
    border-radius: 3px;
}

input[type=range]::-webkit-slider-thumb {
    -webkit-appearance: none;
    height: 40px;
    width: 40px;
    border-radius: 50%;
    background: var(--clr-StrongCyan);
    background-image: url('/images/icon-slider.svg');
    background-repeat: no-repeat;
    background-position: center;
    cursor: pointer;
    margin-top: -15px;
    box-shadow: 1px 1px 1px var(--clr-SoftCyan), 0px 0px 10px var(--clr-SoftCyan); 
}

input[type=range]::-moz-range-thumb {
    height: 40px;
    width: 40px;
    border-radius: 50%;
    background: var(--clr-StrongCyan);
    background-image: url('/images/icon-slider.svg');
    background-repeat: no-repeat;
    background-position: center;
    cursor: pointer;
    margin-top: -15px;
    box-shadow: 1px 1px 1px var(--clr-SoftCyan), 0px 0px 10px var(--clr-SoftCyan); 
}

.box-price .views {
    font-size: 14px;
}

.box-price .price span {
    font-size: 35px;
    color: var(--clr-darkDesaturatedBlue);
}

.box-price .info {
    font-size: 15px;
}

.activ {
    background: var(--clr-lightGrayishBlue);
    border-radius: 15px;
    width: 60px;
    height: 25px;
    position: relative;
    transition: background .5s;
}

.circle {
    background: #fff;
    border-radius: 50%;
    display: inline-block;
    position: absolute;
    width: 20px;
    height: 20px;
    top: 2px;
    transition: all .5s;
}

.active-bg {
    background: var(--clr-StrongCyan);
}

.button {
    background: var(--clr-darkDesaturatedBlue);
    padding: 8px 12px;
    display: inline-block;
    border-radius: 15px;
    margin-top: 10px;
    font-size: 13px;
    color: var(--clr-PaleBlue);
}

.discont {
    color: var(--clr-LightRed);
    background-color: var(--clr-LightGrayishRed);
}
</style>