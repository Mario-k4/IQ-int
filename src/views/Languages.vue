<template>
    <v-app>
        <v-container fluid class="custom-background-lang">
            <v-col xl="12">
                <h1 class="text-h2 font-weight-bold text-white ms-16" id="responsive-naslov">Нудиме преводи </h1>
                <h1 class="text-h3 text-white ms-16" id="responsive-naslov">на следниве јазици </h1>
            </v-col>
        </v-container>
        <!-- order translation banner -->
        <!-- <div id="order">
            <p>
                Нудиме судски и останати преводи на повеќе од 20 јазици
            </p>
            <a href="#"><button>Закажи превод</button></a>
        </div> -->
        <ZakaziPrevod />
        <v-container fluid class="d-flex flex-wrap justify-center pb-16 flags">
            <span>
                <img src="../assets/img/makedonija.jpg">
                <p>Македонски</p>
            </span>

            <span>
                <img src="../assets/img/anglija.jpg">
                <p>Англиски</p>
            </span>

            <span>
                <img src="../assets/img/hrvatska.jpg">
                <p>Хрватски</p>
            </span>

            <span>
                <img src="../assets/img/srbija.jpg">
                <p>Српски</p>
            </span>

            <span>
                <img src="../assets/img/crnagora.jpg">
                <p>Црногорски</p>
            </span>

            <span>
                <img src="../assets/img/germanija.jpg">
                <p>Германски</p>
            </span>

            <span>
                <img src="../assets/img/francija.jpg">
                <p>Француски</p>
            </span>

            <span>
                <img src="../assets/img/bugarija.jpg">
                <p>Бугарски</p>
            </span>

            <span>
                <img src="../assets/img/italija.jpg">
                <p>Италијански</p>
            </span>

            <span>
                <img src="../assets/img/spanija.jpg">
                <p>Шпански</p>
            </span>

            <span>
                <img src="../assets/img/slovenecki.jpg">
                <p>Словенечки</p>
            </span>

            <span>
                <img src="../assets/img/slovacki.jpg">
                <p>Словачки</p>
            </span>

            <span>
                <img src="../assets/img/albanija.jpg">
                <p>Албански</p>
            </span>

            <span>
                <img src="../assets/img/romanija.jpg">
                <p>Романски</p>
            </span>

            <span>
                <img src="../assets/img/holandija.jpg">
                <p>Холандија</p>
            </span>

            <span>
                <img src="../assets/img/turcija.jpg">
                <p>Турски</p>
            </span>

            <span>
                <img src="../assets/img/polska.jpg">
                <p>Полски</p>
            </span>

            <span>
                <img src="../assets/img/ungarija.jpg">
                <p>Унгарски</p>
            </span>

            <span>
                <img src="../assets/img/ceska.jpg">
                <p>Чешки</p>
            </span>

            <span>
                <img src="../assets/img/rusija.jpg">
                <p>Руски</p>
            </span>

            <span>
                <img src="../assets/img/grcija.jpg">
                <p>Грчки</p>
            </span>

            <span>
                <img src="../assets/img/kina.jpg">
                <p>Кинески</p>
            </span>

            <span>
                <img src="../assets/img/arabija.jpg">
                <p>Арапски</p>
            </span>
        </v-container>
        <!-- banner for powerpoint -->
        <div id="banner-hp">
            <p>Изготвување Power point презентации</p>
            <img src="../assets/img/powerpoint-2.svg" alt="Power point logo" id="pp-logo">
        </div>
    </v-app>
</template>
<script>
import ZakaziPrevod from '../components/ZakaziPrevod.vue'
export default {
    name: 'Languages',
    components: {
        ZakaziPrevod
    }
}
</script>
<style>
template {
    font-family: 'Roboto', sans-serif;
}

.custom-background-lang {
    background-image: linear-gradient(180deg, rgba(14, 13, 13, 0) 0%, rgba(14, 13, 13, 0.8) 86.98%),
        url("../assets/img/hero-img-lang.png");
    background-size: cover;
    height: 70vh;
    background-position: center;
    display: flex;
    align-items: center;
}

span img {
    border-radius: 20px;
    width: 289px;
    height: 187px;
    padding: 5px;
}

span p {
    text-align: center;
    padding-bottom: 10px;
}

.flags {
    padding-top: 150px;
    gap: 10px;
}

#order {
    color: #FEFEFE;
    display: flex;
    align-items: center;
    background: linear-gradient(to right, #0C7AA8, #39EDF9);
    border-radius: 10px;
    box-shadow: 0px 4px 4px rgb(0 0 0 / 25%);
    width: 60%;
    justify-content: space-evenly;
    padding: 50px 25px;
    margin: 40px 0;
    position: absolute;
    top: 410px;
    left: 20%;
}

#order p {
    font-size: 22px;
    line-height: 47px;
}

#pp-logo {
    height: 45px;
    padding-left: 30px;
}

#banner-hp {
    color: #FEFEFE;
    display: flex;
    align-items: center;
    background: linear-gradient(to right, #BE4400, #F7AC3B);
    gap: 20px;
    box-shadow: 0px 4px 4px rgb(0 0 0 / 25%);
    width: 100%;
    justify-content: center;
    padding: 20px;
    margin-bottom: 100px;
}

@media screen and (max-width:1090px) {
    #order {
        flex-direction: column;
        gap: 15px;
    }
}

@media screen and (max-width: 780px) {
    #order {
        flex-direction: column;
        gap: 15px;
    }

    span img {
        border-radius: 10px;
        width: 100px;
        height: 70px;
        padding: 5px;
    }
}

@media screen and (max-width: 520px) {
    span img {
        border-radius: 10px;
        width: 100px;
        height: 70px;
        padding: 5px;
    }

    .flags {
        padding-top: 100px;
    }

    #responsive-naslov {
        margin-left: 5px !important;
    }

    #order {
        width: 60%;
        flex-direction: column;
        justify-content: space-between;
        font-size: 14px;
        margin: 30px;
        gap: 15px;
        position: absolute;
        left: 15%;
        top: 470px;
    }

    #order p {
        line-height: 20px;
        font-size: 16px;
        text-align: center;
        display: inherit;
    }
}
</style>