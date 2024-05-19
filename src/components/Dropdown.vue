<template>
  <div class="menu-item d-flex flex-column align-center" @mouseover.native="isOpen = true"
    @mouseleave.native="isOpen = false">
    <!-- @click="isOpen = true" -->
    <!-- @mouseover.native="isOpen = true"
    @mouseleave.native="isOpen = false" -->
    <a href="#" class="d-flex">
      {{ title }}
      <div class=" arrow">></div>
    </a>
    <transition name="fade" appear>
      <div class="sub-menu pb-2" v-if="isOpen">
        <div v-for="(item, i ) in items" :key="i" class="menu-item pb-2">
          <router-link :to="'/services/' + item.title">
            <a @click="handleClose && handleClose()">{{ item.title }}</a>
          </router-link>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'dropdown',
  props: ['title', 'items', 'handleClose', 'isMobile'],
  data() {
    return {
      isOpen: false,
    }
  },
}
</script>
<style>
.arrow {
  rotate: 90deg;
  cursor: pointer;
  padding-left: 3px;
}

.menu-item {
  position: relative;
  display: inline-flex;
  flex-direction: column;
}

.sub-menu {
  width: max-content;
  display: flex;
  flex-direction: column;
  position: absolute;
  top: 170%;
  left: 0;
  background-color: #F6F7F7;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  border-radius: 0px 0px 10px 10px;
  z-index: 1000;
  margin-top: 8px;
  padding: 0px 10px;
}

.menu-item a {
  color: #034763;
  font-size: 14px;
  text-decoration: none;
}

.menu-item a:hover {
  color: #08B2F8;
}

.fade-enter-active,
.fade-leave-active {
  transition: all .3s ease-out;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

@media screen and (max-width: 1090px) {
  .sub-menu {
    top: 120%;
    left: -20%;
    font-size: 11px;
    padding: 0px 5px;
  }
}

@media screen and (max-width: 520px) {
  .sub-menu {
    position: relative;
    background-color: none;
    border-radius: none;
    box-shadow: none;
    align-items: center;
    left: -5%;
  }
}
</style>