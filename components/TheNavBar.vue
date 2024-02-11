<template>
  <nav>
    <ul>
      <li><NuxtLink to="/">داشبورد</NuxtLink></li>
      <li><NuxtLink to="/consumption">مصرفی</NuxtLink></li>
      <li><NuxtLink to="/gym">باشگاه</NuxtLink></li>
      <li><NuxtLink to="/absorption">تغذیه</NuxtLink></li>
      <li><NuxtLink to="/profile">پروفایل</NuxtLink></li>
    </ul>
  </nav>
</template>

<style>
nav {
  font-size: var(--h4-5);
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: rgb(253, 253, 253);
  box-shadow: var(--shadow-1);
}
nav ul {
  display: flex;
  justify-content: space-evenly;
}
nav ul li {
  width: 3.5rem;
  height: 3.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
nav ul li a {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
nav ul li a.router-link-active {
  color: var(--secondary-color);
}
nav ul li a::before {
  font-family: "FontAwesome Solid";
  font-size: 1.3rem;
  align-self: center;
  margin-bottom: 0.2rem;
}
nav ul li a[href="/"]::before {
  content: "\f015";
}
nav ul li a[href="/consumption"]::before {
  content: "\f554";
}
nav ul li a[href="/gym"]::before {
  content: "\f44b";
}
nav ul li a[href="/absorption"]::before {
  content: "\e43f";
}
nav ul li a[href="/profile"]::before {
  content: "\f007";
}
</style>
