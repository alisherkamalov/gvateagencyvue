<template>
  <div class="container">
    <ul class="advantages-ul">
      <li class="email-li">
        <img src="/send-email.svg" />
        Оперативный ответ на заявки
      </li>
      <li class="find-li">
        <img src="/analytics.svg" />
        Улучшаем сайт для поисковых систем
      </li>
      <li class="antivirus-li">
        <img src="/antivirus.svg" />
        Защита сайта от вирусов
      </li>
      <li class="cache-li">
        <img src="/backup.svg" />
        Ежедневное резервное копирование сайта
      </li>
      <li class="always-li">
        <img src="/browsers.svg" />
        Бесперебойная работа сайта 24/7
      </li>
    </ul>
  </div>
</template>

<script>


</script>

<style scoped>
@keyframes advantage {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
    }
}
.container {
  width: 100%;
  height: auto;
  display: flex;
  margin-top: 25px;
  justify-content: center;
}
.advantages-ul {
  height: 120px;
  display: flex;
  gap: 35px;
  position: relative;
  left: -20px;
  flex-wrap: wrap;
  justify-content: center;
}
.email-li {
  display: flex;
  flex-direction: column;
  font-family: "Manrope";
  font-size: 17px;
  font-weight: 300;
  width: 170px;
  line-height: 23.22px;
  text-align: center;
  animation: advantage linear;
  animation-timeline: view();
  animation-range: entry 0;
}
.find-li {
  display: flex;
  flex-direction: column;
  font-family: "Manrope";
  font-size: 17px;
  font-weight: 300;
  width: 170px;
  line-height: 23.22px;
  text-align: center;
  animation: advantage linear;
  animation-timeline: view();
  animation-range: entry 0;
}
.antivirus-li {
  display: flex;
  flex-direction: column;
  font-family: "Manrope";
  font-size: 17px;
  font-weight: 300;
  width: 170px;
  line-height: 23.22px;
  text-align: center;
  animation: advantage linear;
  animation-timeline: view();
  animation-range: entry 0;
}
.cache-li {
  display: flex;
  flex-direction: column;
  font-family: "Manrope";
  font-size: 17px;
  font-weight: 300;
  width: 200px;
  line-height: 23.22px;
  text-align: center;
  animation: advantage linear;
  animation-timeline: view();
  animation-range: entry 0;
}
.always-li {
  display: flex;
  flex-direction: column;
  font-family: "Manrope";
  font-size: 17px;
  font-weight: 300;
  width: 200px;
  line-height: 23.22px;
  text-align: center;
  animation: advantage linear;
  animation-timeline: view();
  animation-range: entry 0;
}
</style>
