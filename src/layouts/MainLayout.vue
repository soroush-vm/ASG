<template>
  <q-layout view="hHh Lpr lFf">
    <!-- <q-header elevated class="bg-blue-grey-6">
      <q-toolbar>
        <q-btn flat dense round icon="menu" aria-label="Menu" @click="toggleLeftDrawer" />
      </q-toolbar>
    </q-header> -->

    <q-drawer
      v-model="drawer"
      :mini="miniState"
      :width="200"
      show-if-above
      :breakpoint="700"
      :mini-width="70"
      @mouseenter="miniState = false"
      @mouseleave="miniState = true"
      mini-to-overlay
      class="text-black"
      :class="[$q.dark.isActive ? 'bg-grey-9' : 'bg-brand']"
    >
      <q-img
        v-if="!miniState"
        class="absolute-top"
        src="../assets/logo.png"
        style="height: 150px"
      />
      <q-img
        v-if="miniState"
        class="absolute-top q-mt-lg"
        src="../assets/minilogo.png"
        style="height: 50px"
      />
      <q-list
        :style="{
          height: 'calc(100% - 150px)',
          marginTop: miniState ? '80px' : '150px',
        }"
      >
        <q-item
          clickable
          v-ripple
          name="dashboard"
          :style="{ backgroundColor: activeTab === 'dashboard' ? '#3b475f' : '#1f2a40' }"
          @click="activeTab = 'dashboard'"
          to="/"
          exact
        >
          <q-item-section avatar>
            <q-icon name="dashboard" color="grey-6" />
          </q-item-section>
          <q-item-section class="text-grey-6">Dashboard</q-item-section>
        </q-item>

        <q-item
          clickable
          v-ripple
          name="about"
          :style="{ backgroundColor: activeTab === 'about' ? '#3b475f' : '#1f2a40' }"
          @click="activeTab = 'about'"
          to="/about"
        >
          <q-item-section avatar>
            <q-icon name="person" color="grey-6" />
          </q-item-section>
          <q-item-section class="text-grey-6">about</q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <!-- <q-btn dense flat icon="menu" @click="mini = !mini" /> -->

    <q-page-container class="bg-body">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const drawer = ref(false)
const miniState = ref(false)
const activeTab = ref('dashboard')
// const leftDrawerOpen = ref(false)
// const toggleLeftDrawer = () => {
//   // miniState.value = true
//   drawer.value = true
// }
// const drawerClick = (e) => {
//   if (miniState.value) {
//     miniState.value = false
//     e.stopPropagation()
//   }
// }
</script>
<style lang="sass">
.my-menu-link
  color: white
  background: #607d8b
</style>
