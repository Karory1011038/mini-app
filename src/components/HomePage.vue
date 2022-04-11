<template>
  <el-container class="common-layout" direction="vertical">
    <el-main style="padding: 20px 10px">
      <el-row :gutter="20">
        <el-col :span="24" class="p-2">
          <h3 class="t1">Добро пожаловать в ИЖС Маркет!</h3>
        </el-col>
        <el-col :span="12" class="pa-0">
          <div class="t-blocks bgc-1">
            <div class="t-text">Выберите проект дома, а разные
              застройщики предложат цены
            </div>
          </div>
        </el-col>
        <el-col :span="12" class="pa-0">
          <div class="t-blocks bgc-2">
            <el-icon class="question">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                   class="bi bi-question-circle" viewBox="0 0 16 16">
                <path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14zm0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16z"/>
                <path
                    d="M5.255 5.786a.237.237 0 0 0 .241.247h.825c.138 0 .248-.113.266-.25.09-.656.54-1.134 1.342-1.134.686 0 1.314.343 1.314 1.168 0 .635-.374.927-.965 1.371-.673.489-1.206 1.06-1.168 1.987l.003.217a.25.25 0 0 0 .25.246h.811a.25.25 0 0 0 .25-.25v-.105c0-.718.273-.927 1.01-1.486.609-.463 1.244-.977 1.244-2.056 0-1.511-1.276-2.241-2.673-2.241-1.267 0-2.655.59-2.75 2.286zm1.557 5.763c0 .533.425.927 1.01.927.609 0 1.028-.394 1.028-.927 0-.552-.42-.94-1.029-.94-.584 0-1.009.388-1.009.94z"/>
              </svg>
            </el-icon>
            <div class="t-text">Выберите проект дома, а разные
              застройщики предложат цены
            </div>
          </div>
        </el-col>
      </el-row>
    </el-main>
    <el-row class="main-block mt-5 pd-0">
      <el-col :span="24">
        <el-scrollbar>
          <div class="scrollbar-flex-content mt-20">
            <span class="scrollbar-demo-item-wrap" v-for="item in scrollBarItems"
                  :class="item.active? 'scrollbar-demo-item-active' : ''" :key="item.text">
            <el-card :style="{ 'background-image': 'url(' + item.href + ')','background-size': '100% auto'}"
                     :body-style="{ padding: '60px 5px 5px 10px'}"
                     class="scrollbar-demo-item">
              <div>
            <p class="scrollbar-demo-item-text">{{ item.text }}</p>
          </div>
            </el-card>
              </span>
          </div>
        </el-scrollbar>
      </el-col>
      <el-col :span="24" style="padding: 20px 10px 0 10px">
        <h3 class="geoposition">Московская область
          <hr class="hr-dashed">
        </h3>
      </el-col>
      <el-col :span="24">
        <el-scrollbar>
          <div class="scrollbar-flex-content p-5">
            <p v-for="item in testScrollItems" :key="item" class="scrollbar-demo-item-two">
              {{ item }}
            </p>
          </div>
        </el-scrollbar>
      </el-col>
      <el-col :span="24">
        <el-row>
          <el-col
              v-for="(o) in 7"
              :key="o"
              :span="12"
              :class="o % 2 === 0 ? 'left-item' : 'right-item'"
          >
            <el-card shadow="always" style="position: relative" class="item-card"
                     :body-style="{ padding: '0px' , 'border-radius': '20px'}">
              <img
                  src="https://cstor.nn2.ru/blog/data/blog/2018-09/32a431f-2018-09-01-Design-of-houses-in-a-modern-style-124.jpg"
                  class="image"
              />
              <el-icon class="more">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor"
                     class="bi bi-three-dots-vertical" viewBox="0 0 16 16">
                  <path
                      d="M9.5 13a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0zm0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0z"/>
                </svg>
              </el-icon>
              <div style="padding: 11px; overflow: hidden">
                <span class="card-title">Название проекта</span>
                <div class="bottom">
                  <span class="card-text">180 м2 | 6-8,9 млн ₽</span>
                </div>
              </div>
            </el-card>
          </el-col>
        </el-row>
        <!--        <el-space wrap style="margin-left: 5px">-->
        <!--          <el-card shadow="always" :body-style="{ padding: '0px' , 'border-radius': '20px'}" v-for="i in 6" :key="i"-->
        <!--                   class="box-card" style="width: 175px">-->
        <!--            <img-->
        <!--                src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png"-->
        <!--                class="image"-->
        <!--            />-->
        <!--            <div style="padding: 14px">-->
        <!--              <span class="card-title">Название проекта</span>-->
        <!--              <div class="bottom">-->
        <!--                <span class="card-text">180 м2 | 6-8,9 млн ₽</span>-->
        <!--              </div>-->
        <!--            </div>-->
        <!--          </el-card>-->
        <!--          <el-card shadow="always" :body-style="{ padding: '0px' , 'border-radius': '20px'}">-->

        <!--          </el-card>-->
        <!--        </el-space>-->
      </el-col>
    </el-row>
  </el-container>
</template>

<script>
import {ref} from 'vue'

export default {
  name: 'HomePage',
  components: {},
  setup() {
    let model = null
    let elementList = ref([{
      name: '',
      active: false
    }, {
      name: '',
      active: false
    },])
    const currentDate = ref(new Date())
    return {model, currentDate, elementList}
  },
  data: () => ({
    testScrollItems: [
      'все — 250',
      'вахверк — 36',
      'клееный брус — 52',
      'газобетон — 42',
    ],
    scrollBarItems: [
      {
        text: 'Экспертиза \nработ',
        href: 'https://yt3.ggpht.com/ytc/AKedOLTRewvfIIgmOSQUgYBmfgdjLJdgC4QuCnmXy28o=s900-c-k-c0x00ffffff-no-rj',
        active: true,
      },
      {
        text: 'Дом\nBLYSKÄR',
        href: 'https://gallery.forum-grad.ru/files/2/6/1/9/lakefront-villa-design-romania-08.jpg',
        active: true,
      },
      {
        text: 'Нас не просили,\nно мы сделали',
        href: 'https://vestirama.ru/assets/templates/images/photo/dcafa5618e871b283fe44861bcc2393e.jpg',
      },
      {
        text: 'Инстаграмная \nлестница',
        href: 'https://i.pinimg.com/originals/16/be/6e/16be6eab12608652d657944428f88831.jpg',
      }
    ],
  }),
}
</script>

<style>
@import url("~@/assets/fonts/mont/stylesheet.css");


.t1 {
  font-family: 'Mont', serif;
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 31px;
  width: 70%;

  color: #FFFFFF;
}

.geoposition {
  display: inline-block;
  font-family: 'Mont', serif;
  font-style: normal;
  font-weight: 800;
  font-size: 18px;
  line-height: 23px;
  color: #000000;
  margin: 0;
}

.t-blocks {
  background: linear-gradient(135.55deg, #A7A6CB -5.43%, #8989BA 107.62%);
  border-radius: 10px;
  position: relative;
}


.question {
  position: absolute;
  right: 12.5%;
  top: 12.5%;
  bottom: 12.5%;
  opacity: 0.5;
  color: #FFFFFF;
}

.bgc-1 {
  /*background: linear-gradient(135.55deg, #A7A6CB -5.43%, #8989BA 107.62%);*/
  background: url('/src/assets/pictures/b1.png');
  background-size: 100% 100%
}

.bgc-2 {
  /*background: linear-gradient(134.43deg, #C79081 26.26%, #DFA579 105.21%);*/
    background: url('/src/assets/pictures/b2.png');
  background-size: 100% 100%

}

.custom {
  z-index: 3;
  position: absolute;
  width: 30%;
  height: 50%;
  left: 112px;
  top: 8px;

  background: linear-gradient(135.3deg, #8989BA 7.36%, #A7A6CB 101.97%);
  filter: blur(8px);
}

.t-text {
  font-family: 'Mont';
  font-style: normal;
  font-weight: 400;
  font-size: 10px;
  line-height: 13px;
  color: #FFFFFF;
  padding: 50px 15px 10px 15px;
}

.main-block {
  background-color: white;
  border-radius: 15px 15px 0 0;
}

.scrollbar-flex-content {
  display: flex;
}

.mt-20{
    margin-top: 20px;
}

.p-5 {
  padding: 5px;
}

.scrollbar-demo-item {
  flex-shrink: 0;
  align-items: center;
  justify-content: center;
  width: 95px;
  height: 95px;
  border-radius: 10px;
  background: var(--el-color-danger-light-9);
  color: var(--el-color-danger);
}

.scrollbar-demo-item-wrap {
  margin: 9px;
  padding: 1px;
}

.scrollbar-demo-item-active {

  border-radius: 12px;
  border: 2px solid #A7A6CB;
}


.scrollbar-demo-item-text {
  white-space: pre-line;
  font-family: 'Mont';
  font-style: normal;
  font-weight: 400;
  font-size: 9px;
  line-height: 115%;
  color: #FFFFFF;
}

.scrollbar-demo-item-two {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: row;
  padding: 0 8px;
  margin: 5px;
  color: #72767A;

  position: static;
  height: 28px;
  left: 182px;
  top: 0;
  font-family: 'Mont';
  font-style: normal;
  font-weight: 600;
  font-size: 11px;
  line-height: 14px;
  /* identical to box height */

  text-align: center;

  border: 1px solid #D7D7D7;
  border-radius: 11px;
}

.hr-dashed {
  margin: 5px 0;
  padding: 0;
  height: 0;
  border: none;
  border-top: 2px dashed #000;
}

.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 3px;
  line-height: 12px;
  justify-content: space-between;
  align-items: center;
}


.item-card{
  width: 175px;
  height: 175px;
  border-radius: 10px 10px;

}
.item-card img {
  width: 100%;
  height: 117px;
  object-fit: cover;
  object-position: 0 0;
}

.image {
  max-width: 100%;
  display: block;
}

.more {
  position: absolute;
  right: 5%;
  top: 5%;
}

.left-item {
  padding: 5px 10px 5px 2px;
}

.right-item {
  padding: 5px 2px 5px 10px;
}

.card-title {
  font-family: 'Mont';
  font-style: normal;
  font-weight: 800;
  font-size: 12px;
  line-height: 15px;
}

.card-text {
  font-family: 'Mont';
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
}
</style>
