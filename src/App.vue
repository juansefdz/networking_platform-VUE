<template>
  <Header />
  <UserBanner />
  <ButtonsZone :selectedButton="selectedButton" @update:selectedButton="updateSelectedButton" />
  <MainZone :currentView="currentViewComponent" />
  <Footer />
</template>

<script setup>
import { ref, computed } from 'vue';
import Header from "@/components/Header.vue";
import UserBanner from "@/components/UserBanner.vue";
import ButtonsZone from "@/components/Buttons-zone.vue";
import MainZone from "@/components/Main-zone.vue";
import Profile from '@/components/ProfileZone/Profile.vue';
import Team from '@/components/TeamZone/Team.vue';
import Footer from '@/components/Footer.vue';
import ConnectionsUsers from '@/components/ConnectionZone/ConnectionUsers.vue';
import ProjectsZone from '@/components/ProjectsZone/Projects.vue';

const selectedButton = ref(0);
const buttons = ref([
  { label: 'Profile', component: Profile },
  { label: 'Team', component: Team},
  { label: 'Projects', component: ProjectsZone },
  { label: 'Connections', component: ConnectionsUsers }
]);

const updateSelectedButton = (index) => {
  selectedButton.value = index;
};

const currentViewComponent = computed(() => buttons.value[selectedButton.value].component);
</script>

<style scoped>

</style>