<template>
  <div class="navigation">
    <div class="container">
      <ul class="top-nav">
        <ul class="burger-button" @click="burgerMenu">
          <li class="line-one"></li>
          <li class="line-two"></li>
          <li class="line-three"></li>
        </ul>
        <img src="/logo.svg" class="logo" alt="логотип gvate agency" />

        <li class="location-li">
          <img src="/location_ico.svg" class="map_ico" alt="иконка локации" />
          Санкт-Петербург, ул. 4-ая Советская, 15/Б
        </li>
        <li class="contact-li">
          <img src="/phone_ico.svg" class="phone_ico" alt="иконка телефона" />
          +7 (812) 424-56-99
        </li>
        <li class="soc-net-li">
          <img src="/wa_ico.svg" alt="иконка whatsapp" />
          <img src="/tg_ico.svg" alt="иконка telegram" />
          <button class="button-contact">Заказать звонок</button>
        </li>
        <img src="/phone_ico.svg" class="phone_ico_mob" alt="иконка телефона" />
      </ul>
    </div>
  </div>
  <div class="line-navigation">
    <div class="container"></div>
  </div>
  <div class="navigation-menu">
    <div class="container">
      <ul class="menu-ul">
        <li class="about-li">
          <RouterLink to="/about" class="router">О нас</RouterLink>
        </li>
        <li class="site-li">
          <RouterLink to="/new-sites" class="router"
            >Создание сайтов</RouterLink
          >
        </li>
        <li class="marketing-li">
          <RouterLink to="/marketing" class="router"
            >Маркетинг и продвижение</RouterLink
          >
        </li>
        <li class="accom-li">
          <RouterLink to="/accom" class="router"
            >Сопровождение сайтов</RouterLink
          >
        </li>
        <li class="portfolio-li">
          <RouterLink to="portfolio" class="router">Портфолио</RouterLink>
        </li>
        <li class="prices-li">
          <RouterLink to="/prices" class="router">Цены</RouterLink>
        </li>
        <li class="contacts-li">
          <RouterLink to="/contacts" class="router">Контакты</RouterLink>
        </li>
      </ul>
    </div>
  </div>
  <div>
    <div class="container">
      <div
        class="burger-menu-white"
        :style="{
          left: this.leftmenu + 'px',
        }"
      >
        <img src="/logo.svg" class="logo-mob" alt="логотип gvate agency" />

        <button class="close-burger-menu" @click="burgerMenu">
          <svg
            class="close-ico"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 384 512"
          >
            <!--!Font Awesome Free 6.6.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.-->
            <path
              fill="#ffffff"
              d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"
            />
          </svg>
        </button>
        <ul class="menu-ul-mob">
          <li class="about-li">
            <RouterLink to="/about" class="router">О нас</RouterLink>
          </li>
          <li class="site-li">
            <RouterLink to="/new-sites" class="router"
              >Создание сайтов</RouterLink
            >
          </li>
          <li class="marketing-li">
            <RouterLink to="/marketing" class="router"
              >Маркетинг и продвижение</RouterLink
            >
          </li>
          <li class="accom-li">
            <RouterLink to="/accom" class="router"
              >Сопровождение сайтов</RouterLink
            >
          </li>
          <li class="portfolio-li">
            <RouterLink to="portfolio" class="router">Портфолио</RouterLink>
          </li>
          <li class="prices-li">
            <RouterLink to="/prices" class="router">Цены</RouterLink>
          </li>
          <li class="contacts-li">
            <RouterLink to="/contacts" class="router">Контакты</RouterLink>
          </li>
        </ul>
      </div>
      <div
        class="black-bg"
        :style="{
          opacity: this.opacityblack,
          pointerEvents: this.pointerblack,
        }"
        @click="burgerMenu"
      ></div>
    </div>
  </div>
</template>

<script>
import { RouterLink } from "vue-router";
export default {
  data() {
    return {
      IsOpen: false,
      leftmenu: -250,
      opacityblack: 0,
      pointerblack: "none",
    };
  },
  methods: {
    burgerMenu() {
      this.IsOpen = !this.IsOpen;
      console.log(this.IsOpen);
      if (this.IsOpen === true) {
        this.leftmenu = 0;
        this.opacityblack = 0.5;
        this.pointerblack = "visible";
      } else {
        this.leftmenu = -250;
        this.opacityblack = 0;
        this.pointerblack = "none";
      }
    },
  },
};
</script>

<style>
.close-burger-menu {
  width: 40px;
  height: 40px;
  border-radius: 10px;
  position: absolute;
  right: 15px;
  top: 17px;
  border: 0;
  cursor: pointer;
  background-color: #d93a4d;
}
.close-ico {
  scale: 0.7;
}
.logo-mob {
  margin-left: 15px;
  margin-top: 15px;
  width: 150px;
}
.burger-menu-white {
  height: 100dvh;
  width: 250px;
  background-color: white;
  display: flex;
  position: fixed;
  top: 0px;
  left: 0px;
  z-index: 101;
  overflow: hidden;
  flex-direction: column;
  gap: 15px;
  transition: all 0.5s ease;
}
.black-bg {
  width: 100%;
  height: 100dvh;
  position: fixed;
  top: 0px;
  right: 0px;
  z-index: 99;
  cursor: pointer;
  background-color: black;
  transition: all 0.5s ease;
}
nav {
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;
}
.container {
  width: 1086px;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.line-one {
  width: 25px;
  height: 2px;
  background-color: #282a2b;
  position: absolute;
  top: -5px;
  margin-top: 25px;
  opacity: 0.5;
}
.line-two {
  width: 25px;
  height: 2px;
  background-color: #282a2b;
  position: absolute;
  top: -15px;
  margin-top: 25px;
  opacity: 0.5;
}
.line-three {
  width: 25px;
  height: 2px;
  background-color: #282a2b;
  position: absolute;
  top: 5px;
  margin-top: 25px;
  opacity: 0.5;
}
.map_ico {
  width: 24px;
  height: 24px;
}
.burger-button {
  width: 80px;
  height: 50px;
  display: none;
  position: relative;
  top: 3px;
  cursor: pointer;
}
.about-li {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  transition: all 0.5s ease;
}
.about-li:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.site-li {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  transition: all 0.5s ease;
}
.site-li:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.accom-li {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  transition: all 0.5s ease;
}
.accom-li:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.portfolio-li {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  transition: all 0.5s ease;
}
.portfolio-li:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.prices-li {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  transition: all 0.5s ease;
}
.prices-li:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.contacts-li {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  transition: all 0.5s ease;
}
.contacts-li:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.marketing-li {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  transition: all 0.5s ease;
}
.marketing-li:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.router {
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 500;
  line-height: 25.5px;
  text-align: left;
  gap: 5px;
  color: black;
  text-decoration: none;
  transition: all 0.5s ease;
}
.router:hover {
  color: #d93a4d;
  translate: 0px -5px;
}
.line-navigation {
  width: 100%;
  height: 1px;

  background-color: #282a2b;
  margin-top: 75px;
  margin-bottom: 15px;
  opacity: 0.1;
}
.button-contact {
  width: 136px;
  height: 46px;

  border: 0;
  border-radius: 22.5px;
  background-color: #f0c6cb40;
  color: #d93a4d;
  font-family: "Manrope";
  font-size: 13px;
  font-weight: 600;
  line-height: 21.9px;
  text-align: center;
  transition: all 0.5s ease;
}
.button-contact:hover {
  background-color: #d93a4d;
  color: white;
}
.button-contact:active {
  scale: 0.9;
}
.navigation {
  width: 100%;
  height: 70px;
  position: fixed;
  background-color: white;
  display: flex;
  z-index: 3;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 25px;
}
.navigation-menu {
  width: 100dvh;
  height: 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0;
  justify-content: start;
  gap: 50px;
}
.logo {
  width: 137px;
  height: 41.85px;
  margin-right: 50px;
}
.top-nav {
  display: flex;
  gap: 5px;
  flex-direction: row;
  margin-left: -40px;
}
.menu-ul {
  display: flex;
  gap: 50px;
  flex-direction: row;
  position: relative;
  top: -10px;
  margin-left: -40px;
}
.menu-ul-mob {
  display: flex;
  gap: 15px;
  flex-direction: column;
  margin-left: -40px;
  width: 200px;
  position: absolute;
  top: 60px;
  left: 15px;
}
li {
  display: flex;
  align-items: center;
}
.location-li {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 300;
  gap: 5px;
  margin-right: 10px;
  line-height: 27px;
  text-align: left;
}
.contact-li {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 600;
  gap: 5px;
  margin-right: 10px;
  line-height: 27px;
  text-align: left;
}
.soc-net-li {
  display: flex;
  gap: 10px;
}
@media (min-width: 300px) {
  .burger-button {
    display: flex;
    left: -15px;
  }
  .logo {
    width: 131px;
    height: 32.83px;
    position: relative;
    top: 7px;
    left: -25px;
  }
  .line-navigation {
    margin-bottom: 0px;
  }
  .phone_ico_mob {
    display: flex;
    position: relative;
    left: -25px;
    width: 24px;
    height: 50px;
  }
  .navigation-menu {
    display: none;
  }
  .container {
    width: 100%;
  }
  .contact-li {
    display: none;
  }
  .soc-net-li {
    display: none;
  }
  .location-li {
    display: none;
  }
  .top-nav {
    width: 100%;
    justify-content: space-between;
  }
}
@media (min-width: 1086px) {
  .contact-li {
    display: flex;
  }
  .line-navigation {
    margin-bottom: 15px;
  }
  .soc-net-li {
    display: flex;
  }
  .location-li {
    display: flex;
  }
  .navigation-menu {
    display: none;
  }
  .burger-button {
    display: none;
  }
  .phone_ico_mob {
    display: none;
  }
  .navigation-menu {
    display: flex;
  }
  .container {
    width: 1086px;
  }
}
@media (min-width: 1240px) {
  .line-navigation {
    margin-bottom: 15px;
  }
  .menu-ul {
    margin-left: 0px;
  }
  .logo {
    width: 137px;
    height: 41.85px;
    top: 0px;
    left: 0px;
  }
  .contact-li {
    display: flex;
  }
  .soc-net-li {
    display: flex;
  }
  .location-li {
    display: flex;
  }
  .navigation-menu {
    display: flex;
  }
  .burger-button {
    display: none;
  }
  .phone_ico_mob {
    display: none;
  }
  .container {
    width: 1240px;
    flex-direction: row;
    justify-content: space-between;
  }
  .logo {
    width: 167px;
  }
  .router {
    font-size: 18px;
  }

  .button-contact {
    width: 166px;
    font-size: 15px;
  }
}
</style>
