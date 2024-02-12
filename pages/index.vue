<script setup>
let height = 175;
let weight = 55;
let waist = 71;
let thigh = 51;
let perfect_weight = 69;
let perfect_waist = 75;
let perfect_thigh = 59;

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
        :result="weight / ((height / 100) * (height / 100))"
      />
      <CellCommentator commentator="WHtR" :result="waist / height" />
      <CellCommentator commentator="WHR" :result="waist / thigh" />
    </div>
    <CellSummary
      :height="height"
      :weight="weight"
      :waist="waist"
      :thigh="thigh"
      :perfect_weight="perfect_weight"
      :perfect_thigh="perfect_thigh"
      :perfect_waist="perfect_waist"
    />
    <CellInterpretation
      :height="height"
      :weight="weight"
      :waist="waist"
      :thigh="thigh"
      :perfect_weight="perfect_weight"
      :perfect_thigh="perfect_thigh"
      :perfect_waist="perfect_waist"
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
