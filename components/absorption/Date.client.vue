<template>
  <h3>
    {{ tarikh.toLocale("fa").format("dddd") }}،
    {{ tarikh.toLocale("en").format("D") }}
    {{ tarikh.toLocale("fa").format("MMMM") }}
    {{ tarikh.toLocale("en").format("YYYY") }}
  </h3>
</template>

<script setup>
var tarikh = new persianDate();
</script>
