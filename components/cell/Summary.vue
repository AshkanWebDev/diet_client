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
  <div class="summary">
    <h4>خلاصه وضعیت فردی</h4>
    <h5>قد شما {{ height }} سانتی متر است</h5>
    <ul class="responsive-table">
      <li class="table-header">
        <div class="col col-1">مفسر</div>
        <div class="col col-2">وزن شما</div>
        <div class="col col-3">ایده آل</div>
        <div class="col col-4">فاصله</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="مفسر">BMI</div>
        <div class="col col-2" data-label="وزن شما">{{ weight }} kg</div>
        <div class="col col-3" data-label="ایده آل">
          {{ perfect_weight }} kg
        </div>
        <div class="col col-4" data-label="فاصله">
          {{ weight - perfect_weight }}
          kg
        </div>
      </li>
    </ul>
    <ul class="responsive-table">
      <li class="table-header">
        <div class="col col-1">مفسر</div>
        <div class="col col-2">دور کمر شما</div>
        <div class="col col-3">ایده آل</div>
        <div class="col col-4">فاصله</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="مفسر">WHtR</div>
        <div class="col col-2" data-label="دور کمر شما">{{ waist }} cm</div>
        <div class="col col-3" data-label="ایده آل">{{ perfect_waist }} cm</div>
        <div class="col col-4" data-label="فاصله">
          {{ waist - perfect_waist }} cm
        </div>
      </li>
    </ul>
    <ul class="responsive-table">
      <li class="table-header">
        <div class="col col-1">مفسر</div>
        <div class="col col-2">دور ران شما</div>
        <div class="col col-3">ایده آل</div>
        <div class="col col-4">فاصله</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="مفسر">WHR</div>
        <div class="col col-2" data-label="دور ران شما">{{ thigh }} cm</div>
        <div class="col col-3" data-label="ایده آل">{{ perfect_thigh }} cm</div>
        <div class="col col-4" data-label="فاصله">
          {{ thigh - perfect_thigh }} cm
        </div>
      </li>
    </ul>
  </div>
</template>

<style>
.summary {
}
.summary h4 {
  margin: 0 1.2rem 1rem;
}
.summary h5 {
  margin: 0 1rem 1rem;
}
.summary ul.responsive-table {
  margin: 0 2rem;
}
.summary ul.responsive-table li {
  border-radius: 3px;
  padding: 0.6rem 0.5rem;
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.summary ul.responsive-table li.table-header {
  background-color: var(--tertiary-color);
  font-size: 14px;
  /* text-transform: uppercase; */
  letter-spacing: 0.03em;
}
.summary ul.responsive-table li.table-row {
  background-color: #ffffff;
  box-shadow: 0px 0px 9px 0px rgba(0, 0, 0, 0.1);
}
.summary ul.responsive-table li .col {
  direction: ltr;
  text-align: center;
}
.summary ul.responsive-table li .col-1 {
  flex-basis: 20%;
}
.summary ul.responsive-table li .col-2 {
  flex-basis: 30%;
}
.summary ul.responsive-table li .col-3 {
  flex-basis: 30%;
}
.summary ul.responsive-table li .col-4 {
  flex-basis: 20%;
}
</style>
