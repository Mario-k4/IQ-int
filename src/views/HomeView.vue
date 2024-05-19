<script>
import PowerPoint from '../components/PowerPoint.vue';
import Cards from '../components/Cards.vue';
import ZakaziPrevod from '../components/ZakaziPrevod.vue';

export default {
  name: 'HomeView',
  components: {
    PowerPoint,
    Cards,
    ZakaziPrevod
  }
}
</script>

<template>
  <v-app>
    <v-main>
      <v-container fluid class="d-flex justify-center align-center custom-background">
        <v-row style="max-width:1500px;">
          <v-col lg="7 pa-xl-0 pa-sm-10">
            <h2 class="text-h2 text-white font-weight-medium">7 дена во неделата, </h2>
            <h2 class="text-h2 text-white font-weight-medium pt-5">24 часа дневно</h2>
            <h3 class="text-white my-6 text-h4">Во секое време на секаков јазик</h3>
            <v-btn rounded="xl" size="x-large" elevation="4" class="bg-orange-darken-3 my-6 hidden-md-and-up">
              Закажи превод
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
      <power-point></power-point>
      <v-container fluid class="pa-0 ma-0">
        <v-row class="ma-0 partOne">
          <v-col lg="6" class="pa-0 imageOne">
            <!--<img src="../assets/img/home-page-img1.png" alt="" >-->
          </v-col>
          <v-col lg="6" class="blue ma-0 pa-10 d-flex flex-column justify-center">
            <div class="pa-5 mb-5">
              <h3 class="text-white text-h3 pb-8 font-weight-bold">Обичен превод</h3>
              <p class="text-h6 blue-text font-weight-regular">Превод без заверка на точноста на преводот.</p>
            </div>
            <div class="pa-5 mb-5">
              <h3 class="text-white text-h3 pb-8 font-weight-bold">Судски превод</h3>
              <p class="text-h6 blue-text font-weight-regular">Превод со заверка на точноста на преводот од овластен
                судски преведувач.</p>
            </div>
            <div class="pa-5 mb-5">
              <h3 class="text-white text-h3 pb-8 font-weight-bold">Лектура</h3>
              <p class="text-h6 blue-text font-weight-regular">Проверка на прецизноста на преводот и правилна употреба на
                граматичките и
                правописните
                правила.</p>
            </div>
            <div class="pa-5 mb-5">
              <h3 class="text-white text-h3 pb-8 font-weight-bold">Превод на видео матeријали</h3>
              <p class="text-h6 blue-text font-weight-regular">ТВ програми, веб страни, софтверски решенија.</p>
            </div>
          </v-col>
        </v-row>
        <v-row class="d-flex justify-center align-center">
          <v-col lg="6" class="ma-0 px-lg-15 pa-md-10">
            <div class="pa-5 mb-5">
              <h3 class="text-h3 pb-8 font-weight-bold dark-blue">Адаптација или пресоздавање на текст</h3>
              <p class="text-h6 blue-text font-weight-regular grey">Согласно одредени параметри што се важни за
                одредена целна
                група.</p>
            </div>
            <div class="pa-5 mb-5">
              <h3 class="text-h3 pb-8 font-weight-bold dark-blue">Транскрипција на снимен матeријал</h3>
              <p class="text-h6 blue-text font-weight-regular grey">Аудио запис и негов превод доколку е потребно.</p>
            </div>
            <div class="pa-5 mb-5">
              <h3 class="text-h3 pb-8 font-weight-bold dark-blue">Терминолошки работи</h3>
              <p class="text-h6 blue-text font-weight-regular grey">Изработување на поимници, истражување на специфична
                терминологија.</p>
            </div>
          </v-col>
          <v-col lg="6" class="pa-0">
            <img src="/src/assets/img/home-page-img2.png" class="imageTwo">
          </v-col>
        </v-row>
      </v-container>
      <v-container>
      </v-container>
      <v-container>
        <ZakaziPrevod></ZakaziPrevod>
        <h2 class="text-h2 text-center mb-4 mt-15 font-weight-regular dark-blue">Програма за лојалност</h2>
        <cards></cards>
      </v-container>
      <v-container class="pod-karticki">
        <v-row class="mt-5 d-flex flex-column flex-md-row mx-15">
          <v-col>
            <p class="dark-blue"><span>&#x2022</span> Програмата за лојалност се спроведува на годишно ниво <span
                class="text-decoration-underline">во текот на една
                календарска година.</span>
            </p>
          </v-col>
          <v-col>
            <p class="dark-blue"><span>&#x2022</span> Повратот се пресметува од нето износот на вкупната цена за
              извршениот
              превод.</p>
          </v-col>
        </v-row>
        <v-row class="my-10 d-flex flex-column flex-md-row mx-15">
          <v-col>
            <p class="dark-blue"><span>&#x2022</span> Повратот се пресметува од првиот доставен документ за превод
              од почетокот
              на
              тековната календарска година,
              односно 01 јануари, до крајот на календарската година, односно 31 декември, а повратот на средства се врши
              на
              01 февруари во наредната календарска година за целата претходна календарска година.</p>
          </v-col>
          <v-col>
            <p class="dark-blue"><span>&#x2022</span> За активирање на програмата за лојалност, неопходно е да се
              склучи
              договор за
              минимален период од 1 година
              и
              за обем од минимум 200 страници.</p>
          </v-col>
        </v-row>
      </v-container>
      <power-point></power-point>
    </v-main>
  </v-app>
</template>


<style>
.custom-background {
  background-image: linear-gradient(to bottom, rgba(245, 246, 252, 0.32), rgba(19, 16, 169, 0.53)), url(../assets/img/hero-image-home-page.png);
  background-repeat: no-repeat;
  background-size: cover;
  height: 90vh;
}

.blue {
  background-color: #068EC6;
}

.blue-text {
  color: #9AEDFF;
}

.dark-blue {
  color: #034763;
}

.pod-karticki p {
  font-size: 16px;
}

.grey {
  color: #6C7072;
}

.imageOne {
  background-image: url("../assets/img/home-page-img1.png");
  background-size: cover;
  min-height: 550px !important;
}

.v-row {
  margin: 0 !important;
}

@media screen and (max-width:1279px) {
  .partOne {
    flex-direction: column-reverse;
  }

  .imageTwo {
    max-height: 550px;
  }
}
</style>
