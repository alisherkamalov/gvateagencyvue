<template>
  <div class="header-center">
    <img src="/header-bg.jfif" class="bg-header"/>
    <div class="white-container"></div>
    <div class="left-header"
    :style="{
      translate: this.translateleft,
      opacity: this.opacityimg
    }">
      Комплексное сопровождение сайта
      <span class="text-info"
        >Возьмем на себя все трудности по администрированию любых сайтов
      </span>
      <button class="order-service-btn">Заказать обслуживание</button>
    </div>
    <div class="right-header"
    :style="{
      translate: this.translateimg,
      opacity: this.opacityimg
    }">
      <img src="/header-img.svg" class="img-header" />
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            animate: false,
            translateimg: '100px 0px',
            translateleft: '-100px 0px',
            opacityimg: 0
        };
    },
    methods: {
        Animate() {
            setTimeout(() => {
                this.animate = true;
                if (this.animate) {
                    this.translateimg = '0px 0px';
                    this.translateleft = '0px 0px';
                    this.opacityimg = 1;
                } else {
                    this.translateimg = '100px 0px';
                    this.translateleft = '-100px 0px';
                    this.opacityimg = 0;
                }
            }, 200);
        }
    },
    mounted() {
        this.Animate();
    }
};
</script>


<style>
.header-center {
  width: 1280px;
  height: 600px;
  overflow: hidden;
  display: flex;
  position: relative;
  align-items: start;
  background-color: rgba(255, 255, 255, 0.5);
}
.bg-header {
  width: 100%;
  max-width: 1240px;
  max-height: 100%;
  object-fit: cover;
  z-index: 0;
  top: 0px;
  scale: 5;
  overflow: hidden;
  background-color: white;
  position: absolute;
}
.white-container {
  width: 100%;
  height: 100%;
  background-color: white;
  opacity: 0.95;
  scale: 5;
  overflow: hidden;
  position: absolute;
}
.order-service-btn {
  width: 301px;
  height: 81px;
  padding: 24px 38px 28px 38px;
  gap: 10px;
  border-radius: 8px;
  background-color: #d93a4d;
  color: white;
  border: 0;
  box-shadow: 0px 2.53px 4.44px 0px #e200213c;
  box-shadow: 0px 8.49px 17.17px 0px #e2002158;
  box-shadow: 0px 30px 48px 0px #e200214d;
  font-family: "Manrope";
  font-size: 19px;
  font-weight: 600;
  line-height: 29.45px;
  text-align: left;
  transition: all 0.5s ease;
}
.order-service-btn:hover {
  background-color: white;
  translate: 0px -5px;
  color: #d93a4d;
}
.order-service-btn:active {
  scale: 0.9;
}
.text-info {
  font-family: "Manrope";
  font-size: 24px;
  font-weight: 300;
  display: flex;
  line-height: 36px;
  color: #282a2b;
}
.left-header {
  width: 55%;
  height: 128px;
  gap: 15px;
  display: flex;
  margin-left: 15px;
  margin-right: 15px;
  flex-direction: column;
  padding-top: 100px;
  font-family: "Manrope";
  font-size: 56px;
  font-weight: 800;
  line-height: 64.4px;
  text-align: left;
  transition: all 0.5s ease;
}
.right-header {
  width: 45%;
  position: relative;
  right: -25px;
  top: 50px;
  height: 549px;
  transition: all 0.5s ease;
}
.img-header {
  width:100%;
  scale: 1.4;
  height: 100%;
  pointer-events: none;
}
@media (min-width: 300px) {
  .header-center {
    flex-wrap: wrap;
    height: 800px;
  }
  .left-header {
    font-size: 30px;
    line-height: 35px;
    text-align: center;
    align-items: center;
    width: 100%;
    height: 300px;
    padding-top: 25px;
  }
  .text-info {
    font-size: 20px;
  }
  .right-header {
    width: 100%;
    display: flex;
    height: 300px;
    position: relative;
    top: -90px;
    align-items: center;
    justify-content: center;
  }
  .img-header {
    scale: 1;
    width: 100%;
  }
  header {
    height: 700px;
  }
}
@media (min-width: 600px) {
  header {
    height: 700px;
  }
  .header-center {
    flex-wrap: wrap;
    height: 700px;
  }
  .left-header {
    font-size: 30px;
    line-height: 35px;
    text-align: center;
    align-items: center;
    width: 100%;
    height: 300px;
    padding-top: 25px;
  }
  .text-info {
    font-size: 20px;
  }
  .right-header {
    width: 100%;
    display: flex;
    height: 300px;
    position: relative;
    top: -50px;
    align-items: center;
    justify-content: center;
  }
  .img-header {
    scale: 1.2;
    width: 100%;
  }
}

@media (min-width: 1086px) {
  header {
    height: 600px;
  }
  .header-center {
    overflow: hidden;
    flex-wrap: nowrap;
    width: 100%;
    height: 600px;
  }
  .right-header {
    top: 140px;
    width: 45%;
    right: -15px;
  }
  .img-header {
    scale: 1.5;
    width: 100%;
  }
  .left-header {
    text-align: start;
    align-items: start;
    font-size: 56px;
    width: 55%;
    padding-top: 100px;
    line-height: 64.4px;
  }
  .text-info {
    font-size: 24px;
  }
}
@media (min-width: 1400px) {
  header {
    height: 600px;
  }
  .header-center {
    overflow: visible;
    flex-wrap: nowrap;
    width: 1240px;
    height: 600px;
  }
  .right-header {
    top: 140px;
    width: 45%;
    right: -15px;
  }
  .img-header {
    scale: 1.5;
    width: 100%;
  }
  .left-header {
    text-align: start;
    align-items: start;
    font-size: 56px;
    width: 55%;
    padding-top: 100px;
    line-height: 64.4px;
  }
  .text-info {
    font-size: 24px;
  }
}
</style>
