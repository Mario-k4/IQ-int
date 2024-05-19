<template>
    <v-container fluid class="bg-image d-flex align-end">
        <v-title class="ml-15 pb-3 font-weight-medium hero-title">{{ item ? item : "Нарачај превод" }}</v-title>
    </v-container>
    <Form :item="item"></Form>
</template>
<script>
import Form from '../components/Form.vue'


export default {
    name: 'services',
    components: {
        Form
    },
    // props: ['title'],
    data() {
        return {
            isOpen: false,
            item: null
        }

    },
    watch: {
        '$route.params.item'(newItem) {
            if (!newItem) return;
            this.item = newItem;
        }
    },
    //se izvrsuva na prvo inizilizirajne 
    created() {
        if (!this.$route.params.item) return;
        this.item = this.$route.params.item;
    },

}
</script>
<style>
.bg-image {
    height: 250px;
    background-image: linear-gradient(to bottom, rgba(245, 246, 252, 0.32), rgba(19, 16, 169, 0.53)), url("../assets/img/heroimageuslugi.png");
    background-size: cover;
}

.hero-title {
    font-size: 42px;
    color: #F6F5F5;
}

@media screen and (max-width: 520px) {
    .hero-title {
        font-size: 32px;
        margin-left: 10px !important;
    }
}
</style>
