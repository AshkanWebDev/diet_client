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
    <li v-if="perfect_weight > weight">
      شما دچار {{ perfect_weight - weight }} کیلوگرم کمبود وزن هستید.
    </li>
    <li v-if="perfect_weight == weight">وزن شما دقیقا فیت میباشد.</li>
    <li v-if="perfect_weight < weight">
      شما دچار {{ weight - perfect_weight }} کیلوگرم اضافه وزن هستید.
    </li>
    <li v-if="perfect_waist > waist">شما از ناحیه دور کمر کمبود وزن دارید.</li>
    <li v-if="perfect_waist == waist">دور کمر شما دقیقا فیت هست.</li>
    <li v-if="perfect_waist < waist">شما از ناحیه دور کمر اضافه وزن دارید.</li>
    <li v-if="perfect_thigh > thigh">شما از ناحیه دور ران کمبود وزن دارید.</li>
    <li v-if="perfect_thigh == thigh">دور ران شما دقیقا فیت هست.</li>
    <li v-if="perfect_thigh < thigh">شما از ناحیه دور ران اضافه وزن دارید.</li>
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
