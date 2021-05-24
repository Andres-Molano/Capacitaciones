<template>
  <div>
    <header class="section-header">
    <a href="/" class="section-header-logo">
      <img src="https://i.ibb.co/b6D3Bkn/corona-logo.png" alt="Corona Extra Logo" />
    </a>

    <div class="section-header-menu" id="icon-menu" @click="hola()">
      <div class="section-header-menu__bar section-header-menu--one"></div>
      <div class="section-header-menu__bar section-header-menu--two"></div>
      <div class="section-header-menu__bar section-header-menu--three"></div>
    </div>

    <nav class="section-menu" id="main-nav">
      <ul class="section-menu-main">
        <li class="section-menu-main__item">
          <a href="#" class="section-menu-main__link section-menu-main__link--active">products</a>
        </li>
        <li class="section-menu-main__item">
          <a href="#" class="section-menu-main__link">shop merch</a>
        </li>
        <li class="section-menu-main__item">
          <a href="#" class="section-menu-main__link">about</a>
        </li>
        <li class="section-menu-main__item">
          <a href="#" class="section-menu-main__link">contact</a>
        </li>
      </ul>
    </nav>
  </header>
  </div>
</template>

<script>
export default {
  methods:{
    hola(){
      const iconMenu = document.getElementById("icon-menu");
      const mainNav = document.getElementById("main-nav");
      mainNav.classList.toggle("show-nav");
      iconMenu.classList.toggle("close-menu");
    }
  }
}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;700&display=swap");

.section-header {
  position: fixed;
  width: 100%;
  z-index: 999;
  display: flex;
  align-items: center;
  &-logo{
    padding-left: 0.75rem;
    width: 150px;
  }
  &-menu{
    position: fixed;
    right: 30px;
    cursor: pointer;
    z-index: 100;
    &__bar{
      width: 35px;
      background-color: #fff;
      margin: 5px;
      height: 3px;
    }
    .close-menu &--one{
      background-color: #000;
      transform: rotate(-45deg) translate(-5px, 6px);
    }
    .close-menu &--two{
      opacity: 0;

    }
    .close-menu &--three{
      background-color: #000;
      transform: rotate(45deg) translate(-5px, -6px);
    }
  }
}
.section-menu {
  background-color: rgba(266, 266, 266, 0.8);
  position: absolute;
  right: 0;
  top: 0;
  width: 50%;
  min-height: 92vh;
  display: none;
  justify-content: center;
  align-items: center;
  &-main{
    margin-top: 0;
    margin-bottom: 0;
    padding-left: 0;
    &__item{
      list-style: none;
      padding: 0.75rem;
    }
    &__link{
      text-decoration: none;
      color: #000;
      text-transform: uppercase;
    }
    &.active{
      display: flex;
    }
  }
}
.show-nav {
  display: flex;
}
@media screen and (min-width: 64em) {
  .section-header {
    justify-content: space-between;
    padding: 10px 100px;
    &-menu {
      display: none;
    }
  }
  .section-menu {
    display: flex;
    min-height: 0;
    position: unset;
    width: unset;
    background-color: unset;
    &-main {
      display: flex;
    }
    &-main__link {
      color: var(--primary-color);
      font-size: 0.85em;
    }
    &-main__link--active,
    &-main__link:hover {
      color: var(--split-left);
    }
  }



}
</style>