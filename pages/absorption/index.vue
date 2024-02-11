<template>
  <div class="absorption">
    <h2>جذب کالری</h2>
    <p>
      با توجه به جنسیت، فعالیت روزانه و پارامتر های بدن شما و در نظر گرفتن هدف
      تناسب اندام برای شما سیستم جذب کالری متوسط روزانه 2500 کیلوکالری را میدهد
      تا در مدت 30 روز به آرامی به تناسب اندام خود برسید.
    </p>
    <AbsorptionDate />
    <ul class="responsive-table">
      <li class="table-header">
        <div class="col col-1">وعده</div>
        <div class="col col-2">آیتم های مصرفی</div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="وعده">
          ناشتایی <br />
          <small>200 کالری</small>
        </div>
        <div class="col col-2" data-label="آیتم های مصرفی">
          نمیدونم 1، نمیدونم 2، نمیدونم 3، نمیدونم 4، نمیدونم 5، نمیدونم 6،
          نمیدونم 7، نمیدونم 8
        </div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="وعده">
          صبحانه <br />
          <small>500 کالری</small>
        </div>
        <div class="col col-2" data-label="آیتم های مصرفی">
          نمیدونم 1، نمیدونم 2، نمیدونم 3، نمیدونم 4، نمیدونم 5، نمیدونم 6،
          نمیدونم 7، نمیدونم 8
        </div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="وعده">
          ناهار <br />
          <small>700 کالری</small>
        </div>
        <div class="col col-2" data-label="آیتم های مصرفی">
          نمیدونم 1، نمیدونم 2، نمیدونم 3، نمیدونم 4، نمیدونم 5، نمیدونم 6،
          نمیدونم 7، نمیدونم 8
        </div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="وعده">
          عصرانه <br />
          <small>500 کالری</small>
        </div>
        <div class="col col-2" data-label="آیتم های مصرفی">
          نمیدونم 1، نمیدونم 2، نمیدونم 3، نمیدونم 4، نمیدونم 5، نمیدونم 6،
          نمیدونم 7، نمیدونم 8
        </div>
      </li>
      <li class="table-row">
        <div class="col col-1" data-label="وعده">
          شام <br />
          <small>300 کالری</small>
        </div>
        <div class="col col-2" data-label="آیتم های مصرفی">
          نمیدونم 1، نمیدونم 2، نمیدونم 3، نمیدونم 4، نمیدونم 5، نمیدونم 6،
          نمیدونم 7، نمیدونم 8
        </div>
      </li>
    </ul>
    <div>
      <NuxtLink to="/absorption/weekly">برنامه هفته</NuxtLink>
      <button @click="showModal = true">ثبت حساسیت مواد غذایی</button>
    </div>
    <AbsorptionFoodAllergy
      v-show="showModal"
      @close-modal="showModal = false"
    />
  </div>
</template>

<style>
.absorption {
  margin: 0 1rem;
}
.absorption h2 {
  font-family: "Blabeloo";
  font-size: var(--h2);
  text-align: center;
  margin: 2rem 0 1rem;
}
.absorption p {
  text-align: justify;
  line-height: 1.5rem;
  margin-bottom: 1rem;
}
.absorption h3 {
  font-size: var(--h3);
  text-align: center;
  margin-bottom: 1rem;
}
.absorption ul.responsive-table {
  margin: 0 0.5rem;
}
.absorption ul.responsive-table li {
  border-radius: 3px;
  line-height: 1.3rem;
  padding: 0.6rem 0.5rem;
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.absorption ul.responsive-table li.table-header {
  background-color: var(--tertiary-color);
  font-size: 14px;
  letter-spacing: 0.03em;
}
.absorption ul.responsive-table li.table-row {
  background-color: #ffffff;
  box-shadow: 0px 0px 9px 0px rgba(0, 0, 0, 0.1);
}
.absorption ul.responsive-table li .col {
  text-align: center;
  align-self: center;
}
.absorption ul.responsive-table li .col small {
  font-size: var(--h5);
  line-height: 0.6rem;
}
.absorption ul.responsive-table li .col-1 {
  flex-basis: 20%;
}
.absorption ul.responsive-table li .col-2 {
  flex-basis: 80%;
}
.absorption > div {
  display: flex;
  font-size: 0.83rem;
}
.absorption div a {
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
.absorption div button {
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
