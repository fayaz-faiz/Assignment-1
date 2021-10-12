<template>
  <div class="main">
    <div class="header">&nbsp;<i class="fas fa-shopping-cart"></i> ONEPLUS MOBILES...</div>
    <button v-on:click="goToCart()" class="cartitemheader">
      <i class="fas fa-shopping-cart"></i> <p> {{ cartcounter(c1, c2) }} </p>
    </button>
  </div>
  <div class="container">
    <div class="box">
      <img
        src="https://fdn2.gsmarena.com/vv/pics/oneplus/oneplus-7t-pro-0.jpg"
      />
      <h1 class="boxh1">
       OnePlus 7T Pro 5G McLaren Edition HD1925,  <br />
         US Model <br />
        12GB RAM 256GB ROM - GSM Unlocked  <br />
        120Hz Fluid Display | <br />
        65W Ultra Fast Charge |<br />
        50W Wireless Charge |
      </h1>
      <p class="boxp">
6.67" AMOLED QHD+, 90 Hz Fluid Display,  <br />
         16M colors, 4000mAh Battery <br /><br />
        19.5:9 ratio <br /><br />
        256GB SSD storage¹ <br /><br />
        Smartphone | <br /><br />
        Retina display with True Tone <br /><br />
        3120 x 1440 pixels 516ppi, <br /><br />
        Hasselblad Quad Camera | 65W
      </p>
      <h2 class="boxh2">
        From ₹2500/mo. <br />
        with EMI,**
      </h2>
      <p class="boxp1">or</p>
      <h3 class="boxh3">₹45000</h3>
      <button class="boxbutton" v-on:click="increase">ADD TO CART</button>
      <br><br>
      <div class="button-arranging">
      <button class="boxbutton1" v-on:click="decrease">-</button>
      <h1 class="boxbutton2">{{ counter}}</h1>
      <button class="boxbutton3" v-on:click="increase">+</button>
      </div>
    </div>
    <div class="box">
      <img
        src="https://m.media-amazon.com/images/I/81w9PfjekiL._AC_UY327_FMwebp_QL65_.jpg"
      />
      <h1 class="boxh1">
        OnePlus 9 Pro Pine Green |U.S Version |12GB RAM+256GB |  <br />
        Alexa Built-in<br />
        5G Unlocked Android Smartphone | <br />
        120Hz Fluid Display | <br />
        Hasselblad Quad Camera | 65W Ultra Fast Charge |<br/>
         50W Wireless Charge |


      </h1>
      <p class="boxp">
        OnePlus 9 Pro Pine Green | 5G Unlocked Android Smartphone
        <br /><br />
       | 120Hz Fluid Display | <br /><br />
        Hasselblad Quad Camera | 65W <br /><br />
        Retina display with True Tone <br /><br />
       Ultra Fast Charge | 50W Wireless Charge  <br /><br />
       12GB RAM+256GB | Alexa Built-in
      </p>
      <h2 class="boxh2">
        From ₹3500/mo. <br />
        with EMI,**
      </h2>
      <p class="boxp1">or</p>
      <h3 class="boxh3">₹65000</h3>
      <button class="boxbutton" v-on:click="plus">ADD TO CART</button>
      <br><br>
      <div class="button-arranging">
      <button class="boxbutton1" v-on:click="mines">-</button>
      <h1 class="boxbutton2">{{ counter1 }}</h1>
      <button class="boxbutton3" v-on:click="plus">+</button>
      </div>
    </div>
  </div>
  <div class="totalamount">TOTAL = ₹{{ total(t1, t2) }}</div>
  <button class="totalreset" v-on:click="reset(goout1, goout2)">RESET</button>
  <hr />
</template>
<script>
export default {
  name: "App",
  data: () => {
    return {
      counter: 0,
      counter1: 0,
    };
  },
  methods: {
    increase: function () {
      this.counter++;
    },
    decrease: function () {
      if (this.counter > 0) {
        this.counter--;
      }
    },
    goout1: function () {
      this.counter = 0;
    },
    goout2: function () {
      this.counter1 = 0;
    },
    reset: function (goout1, goout2) {
      goout1();
      goout2();
    },
    plus: function () {
      this.counter1++;
    },
    mines: function () {
      if (this.counter1 > 0) {
        this.counter1--;
      }
    },
    c1: function () {
      this.counter;
    },
    c2: function () {
      this.counter1;
    },
    cartcounter: function () {
      return this.counter + this.counter1;
    },
    t1: function () {
      return this.counter * 45000 ;
    },
    t2: function () {
      return this.counter1 * 65000;
    },
    total: function (t1, t2) {
      return t1() + t2();
    },

    goToCart(){
      this.$router.push('/cart')
    }

  },
};
</script>

<style scoped>

</style>