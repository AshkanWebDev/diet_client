<template>
  <div class="gym">
    <h2>باشگاه</h2>
    <p>
      با توجه به جنسیت شما و راحتی استفاده، بخش بانوان از باشگاه شما حذف شده
      است.
    </p>
    <GymLessons />
  </div>
</template>

<style>
.gym {
  margin: 0 1rem;
}
.gym h2 {
  font-family: "Blabeloo";
  font-size: var(--h2);
  text-align: center;
  margin: 2rem 0 1rem;
}
.gym p {
  line-height: 1.5rem;
  margin-bottom: 1.5rem;
}
</style>

<script setup>
definePageMeta({
  // middleware: "auth",
});
</script>
