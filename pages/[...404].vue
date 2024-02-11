<template>
  <div class="e404">
    <h3>404</h3>
    <h4>با عرض معذرت چنین صفحه&zwnj;ای در سایت وجود ندارد !!!</h4>
    <h5>
      ولی ما میتوانیم با استفاده از موتور جستجوگر سایت تجربه بهتری در اختیار شما
      بگذاریم
    </h5>
  </div>
</template>

<style>
div.e404 {
  margin: 4rem 2rem 3rem;
  text-align: center;
}
div.e404 > h3 {
  direction: ltr;
  font-size: calc(var(--h1) * 3);
  margin-bottom: 1.5rem;
}
div.e404 > h4 {
  font-size: var(--h2);
  margin-bottom: 2.5rem;
  line-height: 2.5rem;
}
div.e404 > h5 {
  font-size: var(--h3);
  line-height: 2rem;
  margin-bottom: 1.5rem;
}
div.e404 > div.search {
  max-width: 62.5rem;
  margin: 0 auto;
}
div.e404 > div.search > div.searchbar {
  display: flex;
}
@media (min-width: 466px) {
  div.e404 {
    margin: 7rem 5rem 6rem;
  }
  div.e404 > h3 {
    margin-bottom: 0.7rem;
  }
  div.e404 > h4 {
    margin-bottom: 1.5rem;
  }
  div.e404 > h5 {
    margin-bottom: 2rem;
  }
}
@media (min-width: 1000px) {
  div.e404 > h3 {
    font-size: calc(var(--h1) * 4);
  }
  div.e404 > h4 {
    font-size: var(--h1);
  }
  div.e404 > h5 {
    font-size: var(--h2);
  }
}
</style>
