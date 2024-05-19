<template>
    <template>
        <div class="text-center">
            <v-menu open-on-hover>
                <template v-slot:activator="{ props }">
                    <a href="#" v-bind="props">
                        {{ title }}
                    </a>
                    >
                </template>
                <v-list class="custom-menu">
                    <v-list-item v-for="(item, i) in items" :key="i" class="menu-item pb-2">
                        <router-link :to="'/services/' + item.title">
                            <a>{{ item.title }}</a>
                        </router-link>
                    </v-list-item>
                </v-list>
            </v-menu>
        </div>
    </template>
</template>
<v-menu @click="isOpen = true">
    <template v-slot:activator="{ props }">
      <div class="hamburger  d-sm-none" v-bind="props">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
      <v-list v-if="isOpen">
        <v-list-item class="d-flex flex-column">
          <router-link :to="{ name: 'home' }">Дома</router-link>
          <router-link :to="{ name: 'services' }">
            <Dropdown title="Услуги" :items="services"></Dropdown>
          </router-link>
          <router-link :to="{ name: 'contact' }">Контакт</router-link>
          <router-link :to="{ name: 'language' }">Јазици</router-link>
          <router-link :to="{ name: 'about' }">За нас</router-link>
        </v-list-item>
      </v-list>
    </template>
  </v-menu>

<v-menu transition="slide-y-transition">
    <template v-slot:activator="{ props }">
      <div class="hamburger  d-sm-none" v-bind="props">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
    </template>
    <v-list>
      <v-list-item class="d-flex flex-column">
        <router-link :to="{ name: 'home' }">Дома</router-link>
        <router-link :to="{ name: 'services' }">
          <Dropdown title="Услуги" :items="services"></Dropdown>
        </router-link>
        <router-link :to="{ name: 'contact' }">Контакт</router-link>
        <router-link :to="{ name: 'language' }">Јазици</router-link>
        <router-link :to="{ name: 'about' }">За нас</router-link>
      </v-list-item>
    </v-list>
  </v-menu>
<script>
</script>
<style></style>