<template>
  <TheNavBar />
  <TheHeader />
  <RouterView style="margin-bottom: 5rem" />
</template>

<style>
.background {
  background: rgb(237, 212, 154);
  background: linear-gradient(
    160deg,
    rgba(237, 212, 154, 1) 0%,
    rgba(240, 227, 198, 1) 29%,
    rgba(239, 235, 227, 1) 100%
  );
}
</style>
