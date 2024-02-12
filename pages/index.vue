<script setup>
const data = await $fetch("/UserData.json");
// let height = 175;
// let weight = 55;
// let waist = 71;
// let thigh = 51;
// let perfect_weight = 69;
// let perfect_waist = 75;
// let perfect_thigh = 59;

useSeoMeta({
  ogTitle: "دستیار هوشمند تغذیه",
  ogDescription: "دستیار تمام کمال تغذیه",
  ogImage: "[og:image]",
  ogUrl: "[og:url]",
  twitterTitle: "[twitter:title]",
  twitterDescription: "دستیار تمام کمال تغذیه",
  // twitterImage: "[twitter:image]",
  twitterCard: "summary",
});
</script>

<template>
  <div>
    <!-- <div> -->
    <div class="index-header">
      <CellCommentator
        commentator="BMI"
        :result="data.weight / ((data.height / 100) * (data.height / 100))"
      />
      <CellCommentator commentator="WHtR" :result="data.waist / data.height" />
      <CellCommentator commentator="WHR" :result="data.waist / data.thigh" />
    </div>
    <CellSummary
      :height="data.height"
      :weight="data.weight"
      :waist="data.waist"
      :thigh="data.thigh"
      :perfect_weight="data.perfect_weight"
      :perfect_thigh="data.perfect_thigh"
      :perfect_waist="data.perfect_waist"
    />
    <CellInterpretation
      :height="data.height"
      :weight="data.weight"
      :waist="data.waist"
      :thigh="data.thigh"
      :perfect_weight="data.perfect_weight"
      :perfect_thigh="data.perfect_thigh"
      :perfect_waist="data.perfect_waist"
    />
  </div>
</template>

<style>
.index-header {
  display: flex;
  justify-content: space-evenly;
  margin: 1rem 0;
}
</style>
