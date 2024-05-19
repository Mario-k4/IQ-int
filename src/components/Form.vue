<template>
    <v-sheet class="d-flex justify-center my-10 mx-5">
        <v-form class="form-background rounded-xl">
            <h3 class="mb-7">Нарачај превод</h3>
            <v-row class="d-flex flex-wrap justify-space-evenly">
                <div class="d-flex flex-column justify-space-between mx-3">
                    <label for="name">Име и презиме</label>
                    <input type="text" name="name" id="name" v-model="name" required>
                    <label for="telefon">Телефон</label>
                    <input type="number" name="number" id="number" v-model="phone" required>
                    <label for="email">Е-маил адреса</label>
                    <input type="email" name="email" id="email" v-model="email" required>
                    <label for="jazik">Изберете јазик на изворниот документ</label>
                    <select name="jazik" id="languages" v-model="sourceLanguage" required>
                        <option v-for="option in languages" :value="option"> {{ option }}</option>
                    </select>
                    <label for="uslugi">Изберете услуги</label>
                    <select name="uslugi" id="uslugi" v-model="services" required>
                        <option v-for="option in serviceOptions" :value="option">{{ option }}</option>
                    </select>
                </div>
                <div class="d-flex flex-column justify-space-between mx-3">
                    <div class="d-flex flex-column">
                        <label for="jazik">Изберете јазик за превод</label>
                        <select name="jazik" id="languagesTran" v-model="targetLanguage" required>
                            <option v-for="option in languagesTranslate" :value="option"> {{ option }}</option>
                        </select>
                        <label for="jazik">Коментари/прашања</label>
                        <textarea v-model="comments" class="textarea"></textarea>
                    </div>
                    <div class="btn-form text-right my-3">
                        <Button @click="submitForm"></Button>
                    </div>
                </div>
            </v-row>
        </v-form>
    </v-sheet>
</template>

<script>
import Button from './Button.vue'
export default {
    name: "Form",
    components: {
        Button
    },
    data() {
        return {
            name: '',
            phone: '',
            email: '',
            sourceLanguage: '',
            targetLanguage: '',
            services: '',
            comments: '',
            languages: [
                'Македонски',
                'Англиски',
                'Хрватски',
                'Српски',
                'Црногорски',
                'Германски',
                'Француски',
                'Бугарски',
                'Италјански',
                'Шпански',
                'Словенечки',
                'Словачки',
                'Албански',
                'Романски',
                'Холандски',
                'Турски',
                'Полски',
                'Унгарски',
                'Чешки',
                'Руски',
                'Грчки',
                'Кинески',
                'Арапски',
            ],
            serviceOptions: [
                'Обичен превод',
                'Судски превод',
                'Превод на видео материјали',
                'Лектура',
                'Адаптација и пресоздавање на текст',
                'Терминолошки работи',
                'Транскрипција на снимен материјал',
                'Изготвување на PowerPoint презентации'
            ],
            languagesTranslate: [
                'Македонски',
                'Англиски',
                'Хрватски',
                'Српски',
                'Црногорски',
                'Германски',
                'Француски',
                'Бугарски',
                'Италјански',
                'Шпански',
                'Словенечки',
                'Словачки',
                'Албански',
                'Романски',
                'Холандски',
                'Турски',
                'Полски',
                'Унгарски',
                'Чешки',
                'Руски',
                'Грчки',
                'Кинески',
                'Арапски',
            ]
        };
    },
    props: ['item'],

    created() {
        this.services = this.item;
    },
    watch: {
        'item'(newitem) {
            this.services = newitem
        }
    },
    methods: {
        submitForm() {
            console.log('Form submitted');
            console.log(this.name, this.phone, this.email, this.sourceLanguage, this.targetLanguage, this.services, this.comments);
        },
    },
};
</script>
<style scoped>
.form-background {
    padding: 30px;
    background-color: #08B2F8;
}

h3 {
    color: #FEFEFE;
    font-size: 24px;
}

.custom-select {
    background-color: #FEFEFE;
    border-radius: 10px;
    border: none;
    width: 370px;
    height: 50px;
}

label {
    color: #FEFEFE;
    font-size: 18px;
    font-weight: 300;
}

input,
select,
textarea {
    width: 370px;
    height: 50px;
    background: #FFFFFF;
    border-radius: 20px;
    border: none;
    margin: 10px 0;
    padding: 0 20px 0 10px;
}

select {
    background-image: url(../assets/img/arrow.png) !important;
    background-repeat: no-repeat;
    background-position: right 12px center;
    background-size: 20px;
}

input:focus,
textarea:focus,
select:focus {
    outline: none;
}

.textarea {
    height: 150px;
    padding-top: 10px !important;
}

@media screen and (max-width: 1090px) {

    input,
    select,
    textarea {
        width: 300px;
    }

    label {
        font-size: 14px;
    }
}
</style>