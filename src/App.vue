<template>
  <header class="position-relative">
      <div class="header-text text-center p-5">
        <h1>Simple, traffic-based pricing</h1>

        <p>
          Sign-up for out 30-day trial. No credit card required.
        </p>
      </div>
  </header>

  <Pricing />
</template>

<script>
import Pricing from './components/Pricing.vue'
export default {
  components: {
    Pricing,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@300;600;800&display=swap');
:root {
  /* (Full Slider Bar) */
  --clr-SoftCyan: hsl(174, 77%, 80%);
  /* (Slider Backround) */
  --clr-StrongCyan: hsl(174, 86%, 45%);
  /* (Discount Background) */
  --clr-LightGrayishRed: hsl(14, 92%, 95%);
  /* (Discount Text) */
  --clr-LightRed: hsl(15, 100%, 70%);
  /* (CTA Text) */
  --clr-PaleBlue: hsl(226, 100%, 87%);

  /* (Pricing Component Background) */
  --clr-white: hsl(0, 0%, 100%);
  /* (Main Background) */
  --clr-veryPaleBlue: hsl(230, 100%, 99%);
  /* (Empty Slider Bar) */
  --clr-lightGrayishBlue: hsl(224, 65%, 95%);
  /* (Toggle Background) */
  --clr-lightBgBlue: hsl(223, 50%, 87%);
  /* (Text) */
  --clr-grayishBlue: hsl(225, 20%, 60%);
  /* (Text & CTA Background) */
  --clr-darkDesaturatedBlue: hsl(227, 35%, 25%);
}

body {
  font-family: 'Manrope', sans-serif;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
}

header {
  height: 25rem;
  width: 100%;
  background-image: url('/images/bg-pattern.svg');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;

  /* background-color: var(--clr-lightGrayishBlue);
  border-bottom-left-radius: 10rem; */
}

header h1 {
  font-size: 21px;
  font-weight: bold;
  color: var(--clr-darkDesaturatedBlue);
}

header p {
  font-size: 15px;
  color: var(--clr-grayishBlue);
}

.header-text {
  background-image: url('/images/pattern-circles.svg');
  background-repeat: no-repeat;
  background-position: center;

  max-width: 400px;
  margin: 0 auto;
}
</style>