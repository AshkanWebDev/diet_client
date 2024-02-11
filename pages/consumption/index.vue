<template>
  <div class="consumption">
    <h2>دفع کالری</h2>
    <p>
      در اینجا قصد ما فقط پی بردن به متوسط دفع کالری روزانه شما را برای کمک کردن
      به بدست آوردن و حفظ کردن آن میباشد
    </p>
    <ul class="responsive-table">
      <li class="table-header">
        <div class="col col-1">روز</div>
        <div class="col col-2">کالری دفعی</div>
        <div class="col col-3">کالری جذبی</div>
        <div class="col col-4">کالری مثبت</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="روز">شنبه</div>
        <div class="col col-2" data-label="کالری دفعی">900 کالری</div>
        <div class="col col-2" data-label="کالری جذبی">1200 کالری</div>
        <div class="col col-2" data-label="کالری مثبت">300 کالری</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="روز">یک&zwnj;شنبه</div>
        <div class="col col-2" data-label="کالری دفعی">800 کالری</div>
        <div class="col col-2" data-label="کالری جذبی">1100 کالری</div>
        <div class="col col-2" data-label="کالری مثبت">300 کالری</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="روز">دوشنبه</div>
        <div class="col col-2" data-label="کالری دفعی">950 کالری</div>
        <div class="col col-2" data-label="کالری جذبی">1200 کالری</div>
        <div class="col col-2" data-label="کالری مثبت">250 کالری</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="روز">سه&zwnj;شنبه</div>
        <div class="col col-2" data-label="کالری دفعی">850 کالری</div>
        <div class="col col-2" data-label="کالری جذبی">1200 کالری</div>
        <div class="col col-2" data-label="کالری مثبت">350 کالری</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="روز">چهارشنبه</div>
        <div class="col col-2" data-label="کالری دفعی">900 کالری</div>
        <div class="col col-2" data-label="کالری جذبی">1200 کالری</div>
        <div class="col col-2" data-label="کالری مثبت">300 کالری</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="روز">پنج&zwnj;شنبه</div>
        <div class="col col-2" data-label="کالری دفعی">800 کالری</div>
        <div class="col col-2" data-label="کالری جذبی">1200 کالری</div>
        <div class="col col-2" data-label="کالری مثبت">400 کالری</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="روز">جمعه</div>
        <div class="col col-2" data-label="کالری دفعی">900 کالری</div>
        <div class="col col-2" data-label="کالری جذبی">1200 کالری</div>
        <div class="col col-2" data-label="کالری مثبت">300 کالری</div>
      </li>
    </ul>
    <div>
      <NuxtLink to="/consumption/weekly">مدیریت هفته</NuxtLink>
      <button @click="showModal = true">ثبت چیت&zwnj;دی</button>
    </div>
    <ConsumptionCheatDay v-show="showModal" @close-modal="showModal = false" />
  </div>
</template>

<style>
.consumption {
  margin: 0 1rem;
}
.consumption h2 {
  font-family: "Blabeloo";
  font-size: var(--h2);
  text-align: center;
  margin: 2rem 0 1rem;
}
.consumption p {
  text-align: justify;
  line-height: 1.5rem;
  margin-bottom: 1.5rem;
}
.consumption ul.responsive-table {
  margin: 0 0.5rem;
}
.consumption ul.responsive-table li {
  border-radius: 3px;
  line-height: 1.3rem;
  padding: 0.6rem 0.5rem;
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.consumption ul.responsive-table li.table-header {
  background-color: var(--tertiary-color);
  font-size: 14px;
  letter-spacing: 0.03em;
}
.consumption ul.responsive-table li.table-row {
  background-color: #ffffff;
  font-size: 14px;
  box-shadow: 0px 0px 9px 0px rgba(0, 0, 0, 0.1);
}
.consumption ul.responsive-table li .col {
  text-align: center;
  align-self: center;
}
.consumption ul.responsive-table li .col-1 {
  flex-basis: calc(calc(100% / 7) * 1.15);
}
.consumption ul.responsive-table li .col-2 {
  flex-basis: calc(calc(100% / 7) * 1.95);
}
.consumption ul.responsive-table li .col-3 {
  flex-basis: calc(calc(100% / 7) * 1.95);
}
.consumption ul.responsive-table li .col-4 {
  flex-basis: calc(calc(100% / 7) * 1.95);
}
.consumption > div {
  display: flex;
  font-size: 0.83rem;
}
.consumption div a {
  display: block;
  margin: 0 auto;
  background-color: var(--tertiary-color);
  color: var(--primary-color);
  border: 0;
  border-radius: 5px;
  padding: 0.6rem 2rem;
  cursor: pointer;
  align-self: center;
}
.consumption div button {
  display: block;
  margin: 0 auto;
  background-color: var(--primary-color);
  color: var(--tertiary-color);
  border: 0;
  border-radius: 5px;
  padding: 0.6rem 2rem;
  cursor: pointer;
  line-height: inherit;
}
</style>

<script>
export default {
  data() {
    return {
      showModal: false,
    };
  },
};
</script>
