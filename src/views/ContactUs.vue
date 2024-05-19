<template>
    <v-app>
        <v-container fluid class="custom-background-contact">
            <v-row>
                <v-col xl="12">
                    <h1 class="text-h2 font-weight-bold text-white ms-16">Контакт</h1>
                </v-col>
            </v-row>
        </v-container>
        <v-container fluid class="back-colour">
            <v-row class="mt-5 mb-5 mx-16 px-16">
                <v-col xl="6">
                    <h2 class="text-h3 font-weight-medium text-white">Контакт податоци</h2>
                    <h4 class="text-h4 text-white pt-10">Контакт</h4>
                    <div class="d-flex my-5">
                        <img src="../assets/img/placeholder-white.png">
                        <p class="ms-5 par-colour">Северна Македонија<br>
                            Ул. 1612 бр. 5-121000 Скопје</p>
                    </div>
                    <div class="d-flex my-5">
                        <img src="../assets/img/telephone-white.png">
                        <p class="ms-5 par-colour"> +389 70 214 551<br>
                            +389 70 786 789</p>
                    </div>
                    <div class="d-flex my-5">
                        <img src="../assets/img/mail-white.png">
                        <p class="ms-5 par-colour">intelligencecenter@outlook.com </p>
                    </div>
                    <div class="d-flex my-5">
                        <img src="../assets/img/clock-white.png">
                        <p class="ms-5 par-colour">Работно време од 08 до 16 часот</p>
                    </div>
                    <h4 class="text-h4 text-white pt-5">Следетене и на: </h4>
                    <div class="mt-3 d-flex icons-gap">
                        <img src="../assets/img/insta_logo.svg">
                        <img src="../assets/img/linkedIn.svg">
                        <img src="../assets/img/facebook.svg">
                    </div>
                </v-col>
                <v-col xl="6">
                    <v-form>
                        <label class="text-white" for="name">Име</label><br>
                        <input type="text" name="name" id="name" v-model="name" required><br>
                        <label class="text-white" for="surname">Презиме</label><br>
                        <input type="surname" name="surname" id="surname" v-model="surname" required>
                        <br>
                        <label class="text-white" for="email">Е-маил адреса</label><br>
                        <input type="email" name="email" id="email" v-model="email" required>
                        <br>
                        <label class="text-white" for="comments">Коментари/Прашања</label><br>
                        <input type="comments" name="comments" id="comments" v-model="comments" required>
                    </v-form>
                    <div class="btn-form">
                        <v-btn class="translateBtn" @click="submitForm">Прати</v-btn>
                    </div>
                </v-col>
            </v-row>
        </v-container>
        <v-row>
            <v-col xl="12">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m16!1m12!1m3!1d6164.864066050676!2d21.473646187982027!3d41.97903470688737!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!2m1!1z0KPQuy4gMTYxMiDQsdGALiA1LTEy!5e0!3m2!1sen!2smk!4v1679071810624!5m2!1sen!2smk"
                    width="100%" height="400" style="border:0;" allowfullscreen="" loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade">
                </iframe>
            </v-col>
        </v-row>

    </v-app>
</template>
<script>
export default {
    data() {
        return {
            name: '',
            surname: '',
            email: '',
            comments: ''
        };
    },
    methods: {
        submitForm() {
            console.log('Form submitted');
            console.log(this.name, this.surname, this.email, this.comments);
        }
    }
}

</script>
<style scoped>
template {
    font-family: 'Roboto', sans-serif;
}

.custom-background-contact {
    background-image: linear-gradient(180deg, rgba(14, 13, 13, 0) 0%, rgba(14, 13, 13, 0.8) 86.98%),
        url("../assets/img/hero-image-contact.png");
    background-size: cover;
    height: 50vh;
    background-position: center;
    display: flex;
    align-items: center;
}

.back-colour {
    background-color: #068EC6;
}

.back-colour img {
    height: 30px;
}

.par-colour {
    color: #034763;
    font-size: 24px;
}

.icons-gap {
    gap: 25px;
}

/* form */
input {
    width: 100%;
    height: 50px;
    background: #FFFFFF;
    border-radius: 20px;
    border: none;
    margin: 10px 0;
    padding: 0 20px 0 10px;
}

input:focus {
    outline: none;
}

#comments {
    width: 100%;
    height: 150px;
}
</style>