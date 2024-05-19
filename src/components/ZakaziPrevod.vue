<template >
    <div class="d-flex justify-center">
        <div class="d-flex my-5 banner-background pa-6 rounded-lg w-75 banner">
            <h1 class="banner-title">Само со еден клик закажете превод</h1>
            <Button></Button>
        </div>
    </div>
</template>
<script>
import Button from '../components/Button.vue'
export default {
    name: 'ZakaziPrevod',
    components: {
        Button
    }
}
</script>
<style>
.banner-background {
    background: linear-gradient(to right, #0C7AA8, #39EDF9);
    box-shadow: 0px 4px 4px rgb(0 0 0 / 25%);
    color: #fefefe;
}

.banner-title {
    font-size: 22px;
    line-height: 47px;
}

.banner {
    justify-content: space-evenly;
}

@media screen and (max-width: 1090px) {
    .banner-title {
        font-size: 18px;
    }

}


@media screen and (max-width: 520px) {
    .banner {
        flex-direction: column;
        width: 60% !important;
        gap: 25px;
    }

    .banner-title {
        line-height: 20px;
        font-size: 16px;
        text-align: center;
    }
}
</style>