<template>
  <nav class="d-flex flex-wrap fixed align-center justify-space-between rounded-xl pa-3 my-6  mx-8">
    <a href="#" class="d-flex"><img src="../assets/img/logo.png" alt="logo"></a>
    <div class="nav-items align-start d-none d-sm-flex">
      <router-link :to="{ name: 'home' }">Дома</router-link>
      <router-link :to="{ name: 'services' }">
        <Dropdown title="Услуги" :items="services"></Dropdown>
      </router-link>
      <router-link :to="{ name: 'contact' }">Контакт</router-link>
      <router-link :to="{ name: 'language' }">Јазици</router-link>
      <router-link :to="{ name: 'about' }">За нас</router-link>
    </div>
    <div class="d-none d-md-block">
      <Button></Button>
    </div>
    <div class="d-flex d-sm-none align-center">
      <button class="hamburger" @click="mobileOpen = !mobileOpen">
        <div class="bar"></div>
        <div class="bar"></div>
        <div class="bar"></div>
      </button>
    </div>
    <!-- Mobile menu -->
    <div class="mobile-menu" v-show="mobileOpen">
      <router-link @click="handleCloseMobileOpen()" :to="{ name: 'home' }">Дома</router-link>
      <router-link :to="{ name: 'services' }">
        <Dropdown title="Услуги" :isMobile="mobileOpen" :handleClose="handleCloseMobileOpen" :items="services"></Dropdown>
      </router-link>
      <router-link @click="handleCloseMobileOpen()" :to="{ name: 'contact' }">Контакт</router-link>
      <router-link @click="handleCloseMobileOpen()" :to="{ name: 'language' }">Јазици</router-link>
      <router-link @click="handleCloseMobileOpen()" :to="{ name: 'about' }">За нас</router-link>
    </div>
  </nav>
</template>
<script>
import Button from './Button.vue'
import Dropdown from './Dropdown.vue';

export default {
  name: 'TheNavbar',
  components: {
    Button,
    Dropdown
  },
  data() {
    return {
      mobileOpen: false,
      services: [
        {
          title: 'Обичен превод',
          link: '#'
        },
        {
          title: 'Судски превод',
          link: '#'
        },
        {
          title: 'Превод на видео материјали',
          link: '#'
        },
        {
          title: 'Лектура',
          link: '#'
        },
        {
          title: 'Адаптација и пресоздавање на текст',
          link: '#'
        },
        {
          title: 'Терминолошки работи',
          link: '#'
        }, {
          title: 'Транскрипција на снимен материјал',
          link: '#'
        },
        {
          title: 'Изготвување на PowerPoint презентации',
          link: '#'
        }
      ],

      title: ""
    }
  },

  methods: {
    handleItemClick(title) {
      console.log(title)
      this.title = title
    },

    handleCloseMobileOpen() {
      this.mobileOpen = !this.mobileOpen
    }
  }
}
</script>
<style scoped>
nav {
  width: -webkit-fill-available;
  background-color: #F6F7F7;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  z-index: 1000;
}

img {
  height: 30px;
}

.mobile-menu {
  position: relative;
  flex-direction: column;
  align-items: center;
  margin-top: 8px;
  padding: 10px;
  width: 100vw;

  display: flex;
}

.mobile-menu a {
  text-decoration: none;
  color: #034763 !important;
  font-size: 14px;
  font-weight: 500;
  margin: 5px;
}

.hamburger {
  background: none;
  border: none;
  padding: 0;
  cursor: pointer;
}

.bar {
  width: 30px;
  height: 3px;
  background-color: #034763;
  margin: 5px;
  transition: all
}

.nav-items a {
  text-decoration: none;
  color: #034763;
  font-size: 14px;
  font-weight: 500;
  padding: 0px 10px;
}

.nav-items a:hover {
  color: #08B2F8;
}

.fixed {
  position: fixed;
}

#arrow {
  background-color: none !important;
}

.hamburger .bar {
  display: block;
  width: 30px;
  height: 3px;
  background-color: #034763;
  margin: 5px;
  -webkit-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}
</style>