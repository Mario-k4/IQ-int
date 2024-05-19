<template>
    <v-app>
        <v-main>
            <v-footer class="set-background" fluid>
                <v-row class="footer-content d-flex flex-wrap justify-space-evenly  py-6 ma-0">
                    <div class="mb-5 .align-self-sm-start">
                        <h4>АЈ ЌУ ИНТЕЛИЏЕНС ДОЕЛ</h4>
                        <div class="socialIcons mt-6">
                            <v-icon class="fab fa-facebook" size="x-large" color="white"></v-icon>
                            <v-icon class="fab fa-instagram" size="x-large" color="white"></v-icon>
                            <v-icon class="fab fa-linkedin" size="x-large" color="white"></v-icon>
                        </div>
                    </div>
                    <div>
                        <h4>Контакт</h4>
                        <div id="companyDescriptionContainer">
                            <div class="d-flex align-center mt-4">
                                <img src="../assets/img/placeholder.png" alt="mapLocation" />
                                <p class="ml-3">Северна Македонија <br />
                                    Ул. 1612 бр. 5-121000 Скопје</p>
                            </div>
                            <div class="d-flex align-center mt-4">
                                <img src="../assets/img/telephone.png" alt="phone" />
                                <p class="ml-3"> +389 70 214 551 <br />
                                    +389 70 786 789</p>
                            </div>
                            <div class="d-flex align-center mt-4">
                                <img src="../assets/img/mail.png" alt="mail" />
                                <p class="ml-3">
                                    <a href="mailto:intelligencecenter@outlook.com">intelligencecenter@outlook.com</a>
                                </p>
                            </div>
                        </div>
                    </div>
                </v-row>
            </v-footer>
        </v-main>
    </v-app>
</template>
<script>
</script>
<style>
.set-background {
    background-color: #068EC6 !important;
}

.set-background img {
    height: 35px;
}

.footer-content {
    padding: 0px 100px !important;
}

h4 {
    color: #034763;
    font-weight: 400;
    font-size: 28px;
}

p,
a {
    color: #F2F3F3;
    font-size: 20px;
}

.v-application__wrap {
    min-height: fit-content !important;
}

@media screen and (max-width: 780px) {
    h4 {
        font-size: 20px;
    }

    p,
    a {
        font-size: 16px;
    }

    .footer-content {
        padding: 10px !important;
    }

    .set-background img {
        height: 30px;
    }
}

@media screen and (max-width: 520px) {
    .footer-content {
        flex-direction: column;
        align-items: flex-start;
        padding: 30px !important;
    }
}
</style>