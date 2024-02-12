<script>
export default {
  props: {
    height: Number,
    weight: Number,
    waist: Number,
    thigh: Number,
    perfect_weight: Number,
    perfect_waist: Number,
    perfect_thigh: Number,
  },
};
</script>

<template>
  <ul class="interpretation">
    <li>تفسیر جدول بالا</li>
    <li>شما دچار 5 کیلوگرم کمبود وزن هستید.</li>

    <li>شما از ناحیه دور کمر هستید.</li>
    <li>شما از ناحیه ران هستید.</li>
  </ul>
</template>

<style>
ul.interpretation {
  margin: 0 1.5rem;
}
ul.interpretation li {
  margin: 0 0.5rem 0.7rem;
  line-height: 1.3rem;
}
ul.interpretation li::before {
  content: "+";
  margin-left: 0.3rem;
}
ul.interpretation li:first-child {
  margin: 0 0 1rem;
}
ul.interpretation li:first-child::before {
  display: none;
}
</style>
