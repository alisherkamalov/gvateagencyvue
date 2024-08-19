<template>
  <div class="container">
    Работы по сопровождению сайта
    <div class="scroll-container">
      <div class="scroll-content">
        <div
          class="item item1"
          @mouseover="toggleAnimation"
          @mouseleave="toggleAnimation"
        >
          <img src="/virus-img.svg" class="img-item" />
          Лечим вирусы
          <span class="span-item">
            Все CMS имеют уязвимости. Лечим зараженные сайты, устраняем «дыры»
            для предотвращения последующих атак злоумышленников.
          </span>
        </div>
        <div
          class="item item2"
          @mouseover="toggleAnimation"
          @mouseleave="toggleAnimation"
        >
          <img src="/error.svg" class="img-item" />
          Находим ошибки
          <span class="span-item">
            Веб сайт может содержать несуществующие страницы, неправильную
            верстку, проблемы с работой модулей на разных устройствах и
            браузерах. Все это устраняем.
          </span>
        </div>
        <div
          class="item item3"
          @mouseover="toggleAnimation"
          @mouseleave="toggleAnimation"
        >
          <img src="/transfer.svg" class="img-item" />
          Переносим сайты
          <span class="span-item">
            При необходимости осуществляем перенос сайта на другой хостинг или
            домен. Делаем это правильно, без негативных последствий для
            поисковых систем.
          </span>
        </div>
        <div
          class="item item4"
          @mouseover="toggleAnimation"
          @mouseleave="toggleAnimation"
        >
          <img src="/design.svg" class="img-item" />
          Дорабатываем дизайн
          <span class="span-item">
            Прорабатываем и внедряем дизайн как интернет сайта полностью, так и
            в отдельности необходимых блоков. Проверяем, чтобы все красиво
            отображалась.
          </span>
        </div>
        <div
          class="item item5"
          @mouseover="toggleAnimation"
          @mouseleave="toggleAnimation"
        >
          <img src="/accommodation.svg" class="img-item" />
          Размещаем информацию
          <span class="span-item">
            Размещаем на веб сайте новую информацию: новости, тексты, товары,
            услуги, цены. Выполняем работы по всему контент-менеджменту.
          </span>
        </div>

        <div
          class="item item6"
          @mouseover="toggleAnimation"
          @mouseleave="toggleAnimation"
        >
          <img src="/admins.svg" class="img-item" />
          Администрируем
          <span class="span-item">
            Администрирование сайта — это внесение мелких правок: меняем
            стоимость услуг/товаров, добавляем/изменяем текста, новости,
            баннеры, картинки и т.д.
          </span>
        </div>
      </div>
    </div>
    <div class="available-cms">
      <span class="text-cms">Мы работаем со всеми популярными CMS</span>
      <div class="images-cms">
        <img
          class="img-cms"
          v-for="(imagecms, index) in imagescms"
          :key="index"
          :src="imagecms.url"
          :style="{
            scale: imagecms.scale,
          }"
        />
      </div>
      <span class="bottom-text-cms">а так же любые самописные CMS</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isPaused: false,
      imagescms: [
        {
          url: "/1c.svg",
          scale: 1,
        },
        {
          url: "/joom.svg",
          scale: 1,
        },
        {
          url: "/drupal.svg",
          scale: 1,
        },
        {
          url: "/wp.svg",
          scale: 1.2,
        },
        {
          url: "/netcat.svg",
          scale: 1,
        },
        {
          url: "/umi.svg",
          scale: 1,
        },
        {
          url: "/opencart.svg",
          scale: 1,
        },
      ],
    };
  },
  methods: {
    toggleAnimation() {
      this.isPaused = !this.isPaused;
      const scrollContent = this.$el.querySelector(".scroll-content");
      console.log(`Animation state: ${this.isPaused ? "paused" : "running"}`);
      scrollContent.style.animationPlayState = this.isPaused
        ? "paused"
        : "running";
    },
  },
};
</script>

<style scoped>
@keyframes escort {
  from {
    opacity: 0.5;
    transform: translateY(-10px) scale(0.9);
  }
  to {
    opacity: 1;
    transform: translateY(0px) scale(1);
  }
}
@keyframes cms {
  from {
    opacity: 0.5;
    transform: translateX(-10px) opacity(0.5);
  }
  to {
    opacity: 1;
    transform: translateX(0px) opacity(1);
  }
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}
.bottom-text-cms {
  font-family: "Manrope";
  font-size: 24px;
  font-weight: 300;
  line-height: 32.78px;
  text-align: center;
}
.img-cms {
  height: 90px;
}
.text-cms {
  font-family: "Manrope";
  font-size: 43px;
  font-weight: 600;
  width: 700px;
  line-height: 58.74px;
  text-align: center;
}
.images-cms {
  width: 100%;
  height: auto;
  display: flex;
  margin-right: 7.5px;
  margin-left: 7.5px;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 35px;
}
.img-item {
  width: 44px;
  height: 36.96px;
}
.span-item {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 300;
  line-height: 22.5px;
  text-align: left;
  color: #282a2b;
}
.scroll-container {
  width: 100%;
  max-width: 1240px;
  overflow: hidden;
  margin-top: 35px;
  position: relative;
  height: 1440px;
  background-color: #fff;
}
.available-cms {
  width: 100%;
  height: auto;
  display: flex;
  gap: 35px;
  padding-top: 25px;
  padding-bottom: 35px;
  background-color: #f9f9f9;
  flex-direction: column;
  align-items: center;
  animation: cms 1s ease-in-out;
  animation-timeline: view();
  animation-range: entry 0;
}

.scroll-content {
  display: flex;
  width: max-content;
  animation: scroll 30s linear infinite;
  gap: 25px;
  padding-top: 15px;
}

.item {
  width: 372px;
  height: 240px;
  background-color: #f0f0f0;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  padding: 25px;
  font-size: 24px;
  color: #333;
  background-color: white;
  border: 0;
  gap: 15px;
  font-family: "Manrope";
  font-size: 20px;
  font-weight: 600;
  line-height: 27.32px;
  text-align: left;
  transition: all 0.5s ease;
}
.item1 {
  border: 1px solid grey;
}
.item2 {
  border: 1px solid grey;
}
.item3 {
  border: 1px solid grey;
}
.item4 {
  border: 1px solid grey;
}
.item5 {
  border: 1px solid grey;
}
.item6 {
  border: 1px solid grey;
}

.item1:hover {
  transform: translateY(-5px);
  box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
}
.item2:hover {
  transform: translateY(-5px);
  box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
}
.item3:hover {
  transform: translateY(-5px);
  box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
}
.item4:hover {
  transform: translateY(-5px);
  box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
}
.item5:hover {
  transform: translateY(-5px);
  box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
}
.item6:hover {
  transform: translateY(-5px);
  box-shadow: rgba(17, 12, 46, 0.15) 0px 48px 100px 0px;
}

.container {
  width: 100%;
  height: 831px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  font-family: "Manrope", sans-serif;
  font-size: 43px;
  font-weight: 600;
  text-align: center;
  line-height: 58.74px;

  animation: escort 1s ease-in-out;
  animation-timeline: view();
  animation-range: entry 0;
}
@media (max-width: 700px) {
  .item {
    width: 200px;
  }
  .container {
    height: 1150px;
  }
  .text-cms {
    font-size: 30px;
    width: 350px;
  }
}
</style>
