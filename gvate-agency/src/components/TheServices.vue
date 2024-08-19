<template>
  <div class="container">
    <div class="content">
      Сколько стоит администрирование сайта?
      <span class="text-info"
        >Тарифы сформированы под объем потребностей и размеры компании
      </span>
      <div class="services-cont">
        <div class="base">
          Базовый
          <span class="price"> 10 000 ₽/мес </span>
          <ul class="base-ul1">
            <li class="base-li1">4 часа работ</li>
            <li class="base-li1">Время реакции: в течение суток</li>
          </ul>
          <div class="line"></div>
          <ul class="base-active">
            Включенные услуги:
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Администрирование сайта
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Мониторинг работоспособности
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Обслуживание сайта (CMS)
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Резервное копирование 1 раз/нед
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Вопросы с тех. службами
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Защита от вирусов
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Критические
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Поддержка электронной почты
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Общие вопросы
            </li>
            <li class="text-active">
              <i class="fa-solid fa-check" style="color: #37ff00"></i>
              Стоимость часа сверх тарифа
            </li>
          </ul>
          <div class="line"></div>
          <div class="hour">
            Час работы сверх пакета:
            <span class="price-hour">2000 ₽/час</span>
            <button class="base-pay">Заказать за 10 000 ₽</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.base-active {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 500;
  line-height: 21px;
  text-align: left;
  margin-left: -40px;
  gap: 25px;
}
.base-pay {
  width: 231px;
  height: 69px;
  display: flex;
  margin-top: 25px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 8px;
  border: 1px solid #fbd6d4;
  color: #d93a4d;
  background-color: white;
  font-family: "Manrope";
  font-size: 17px;
  font-weight: 600;
  line-height: 26.35px;
  text-align: left;
  transition: all 0.5s ease;
}
.base-pay:hover {
  translate: 0px -5px;
  background-color: #d93a4d;
  color: white;
  box-shadow: 0px 2.53px 4.44px 0px #e200213c;

  box-shadow: 0px 8.49px 17.17px 0px #e2002158;

  box-shadow: 0px 30px 48px 0px #e200214d;
}
.hour {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 500;
  line-height: 21px;
  margin-top: 15px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  text-align: left;
}
.price-hour {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 300;
  line-height: 21px;
  text-align: left;
}
.text-active {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 300;
  line-height: 21px;
  margin-top: 10px;
  text-align: left;
  display: flex;
  gap: 5px;
  color: #282a2b;
}
.price {
  font-family: "Manrope";
  font-size: 32px;
  font-weight: 300;
  line-height: 43.71px;
  letter-spacing: -0.02em;
  text-align: left;
}
.line {
  width: 270px;
  height: 1px;
  background-color: #eeeef1;
}
.base {
  width: 299px;
  height: 718px;
  font-family: "Manrope";
  font-size: 20px;
  font-weight: 800;
  line-height: 27.32px;
  text-align: left;
  display: flex;
  flex-direction: column;
}
.base-ul1 {
  margin-left: -37px;
}
.base-li1 {
  font-family: "Manrope";
  font-size: 15px;
  font-weight: 300;
  line-height: 21px;
  text-align: left;
}
.services-cont {
  width: 100%;
  height: 100%;
  display: flex;
}
.container {
  width: 100%;
  height: 867px;
  padding-top: 50px;
  padding-bottom: 50px;
  display: flex;
  justify-content: center;
}
.content {
  width: 100%;
  max-width: 1190px;
  display: flex;
  height: 867px;
  flex-direction: column;
  align-items: center;
  font-family: "Manrope";
  font-size: 43px;
  font-weight: 600;
  line-height: 58.74px;
  text-align: center;
}
.text-info {
  font-family: "Manrope";
  font-size: 24px;
  font-weight: 300;
  line-height: 32.78px;
  text-align: center;
  color: #55585d;
  margin-bottom: 25px;
}
</style>
