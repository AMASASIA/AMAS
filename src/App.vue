<script setup lang="ts">
import { ref } from "vue";
import AmasTop from "./components/AmasTop.vue";
import AmasDashboard from "./components/AmasDashboard.vue";

type View = "home" | "dashboard";
type TabId = "oke" | "communications" | "map" | "finance" | "activation";

const currentView = ref<View>("home");
const activeTab = ref<TabId>("oke");

function goToDashboard(tab: TabId) {
  activeTab.value = tab;
  currentView.value = "dashboard";
}

function backToHome() {
  currentView.value = "home";
}
</script>

<template>
  <div class="min-h-screen">
    <AmasTop
      v-if="currentView === 'home'"
      @select-tab="goToDashboard"
    />
    <AmasDashboard
      v-else
      :initial-tab="activeTab"
      @back-to-home="backToHome"
    />
  </div>
</template>
