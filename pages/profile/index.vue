<script setup>
const data = await $fetch("/UserData.json");
</script>

<script>
export default {
  data() {
    return {
      showDiet: false,
      showDietAttribute: false,
      showBirthday: false,
      showGender: false,
      showHeight: false,
      showWeight: false,
      showThigh: false,
      showWaist: false,
      showHip: false,
      showLogout: false,
    };
  },
};
</script>

<template>
  <div class="profile">
    <div class="image" :class="data.sex">
      <span></span>
    </div>
    <ul>
      <li>
        <p>{{ data.name }} {{ data.lastName }}</p>
      </li>
      <li>
        <div>ایمیل : {{ data.email }}</div>
      </li>
      <li>
        <div>نوع رژیم : همه چیز خوار</div>
        <button @click="showDiet = true">ویرایش</button>
      </li>
      <li>
        <div>تنوع رژیم : برنامه شماره یک</div>
        <button @click="showDietAttribute = true">ویرایش</button>
      </li>
      <li>
        <div>تاریخ تولد : 16 فروردین 1378</div>
        <button @click="showBirthday = true">ویرایش</button>
      </li>
      <li>
        <div v-if="data.sex == 'male'">جنسیت : آقا</div>
        <div v-if="data.sex == 'female'">جنسیت : خانم</div>
        <button @click="showGender = true">ویرایش</button>
      </li>
      <li>
        <div>قد : {{ data.height }} سانتی&zwnj;متر</div>
        <button @click="showHeight = true">ویرایش</button>
      </li>
      <li>
        <div>وزن : {{ data.weight }} کیلوگرم</div>
        <button @click="showWeight = true">ویرایش</button>
      </li>
      <li>
        <div>دور ران : {{ data.thigh }} سانتی&zwnj;متر</div>
        <button @click="showThigh = true">ویرایش</button>
      </li>
      <li>
        <div>دور کمر : {{ data.waist }} سانتی&zwnj;متر</div>
        <button @click="showWaist = true">ویرایش</button>
      </li>
      <li>
        <div>دور باسن : {{ data.hip }} سانتی&zwnj;متر</div>
        <button @click="showHip = true">ویرایش</button>
      </li>
      <li>
        <div>ضریب سوخت و ساز : 1.42</div>
      </li>
      <li>
        <NuxtLink to="/profile/vip">خرید اشتراک</NuxtLink>
      </li>
      <li>
        <div @click="showLogout = true">خروج</div>
      </li>
    </ul>
    <ProfileDiet v-show="showDiet" @close-modal="showDiet = false" />
    <ProfileDietAttribute
      v-show="showDietAttribute"
      @close-modal="showDietAttribute = false"
    />
    <ProfileBirthday
      v-show="showBirthday"
      @close-modal="showBirthday = false"
    />
    <ProfileGender v-show="showGender" @close-modal="showGender = false" />
    <ProfileHeight v-show="showHeight" @close-modal="showHeight = false" />
    <ProfileWeight v-show="showWeight" @close-modal="showWeight = false" />
    <ProfileThigh v-show="showThigh" @close-modal="showThigh = false" />
    <ProfileWaist v-show="showWaist" @close-modal="showWaist = false" />
    <ProfileHip v-show="showHip" @close-modal="showHip = false" />
    <ProfileLogout v-show="showLogout" @close-modal="showLogout = false" />
  </div>
</template>

<style>
.profile .image {
  margin: 1rem auto 20px;
  width: 150px;
  height: 150px;
  box-shadow: 0px 0px 9px 0px rgba(0, 0, 0, 0.1);
  border-radius: 9px;
}
.profile .image.male {
  background-color: rgb(165, 220, 255);
}
.profile .image.female {
  background-color: rgb(255, 211, 234);
}
.profile .image span {
  display: flex;
  width: 100%;
  height: 100%;
  justify-content: center;
  align-items: flex-end;
  font-family: "FontAwesome Solid";
}
.profile .image span::after {
  color: rgba(255, 255, 255, 0.7);
  font-size: 120px;
}
.profile .image.male span::after {
  content: "\e462";
}
.profile .image.female span::after {
  content: "\e463";
}
.profile ul {
  margin: 0 0.5rem;
}
.profile ul li {
  border-radius: 3px;
  line-height: 1.3rem;
  padding: 0.6rem 0.5rem;
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
  background-color: #ffffff;
  box-shadow: 0px 0px 9px 0px rgba(0, 0, 0, 0.1);
}
.profile ul li:first-child {
  margin-bottom: 25px;
  justify-content: center;
}
.profile ul li:nth-last-child(2) {
  justify-content: center;
  background-color: var(--tertiary-color);
  color: var(--primary-color);
}
.profile ul li:last-child {
  justify-content: center;
  background-color: var(--primary-color);
  color: var(--tertiary-color);
}
.profile ul li:last-child div {
  cursor: pointer;
}
.profile ul li button {
  color: inherit;
  background-color: transparent;
  line-height: inherit;
  border: 0;
  padding: 0;
  margin: 0;
  cursor: pointer;
}
</style>
