<script setup lang="ts">
import { ref, watch } from "vue";
import MetricCard from "./MetricCard.vue";
import OkeModule from "@/modules/oke/OkeModule.vue";
import CommModule from "@/modules/communications/CommModule.vue";
import AiMapModule from "@/modules/map/AiMapModule.vue";
import FinanceModule from "@/modules/finance/FinanceModule.vue";
import ActivationModule from "@/modules/activation/ActivationModule.vue";

type TabId = "oke" | "communications" | "map" | "finance" | "activation";

const props = defineProps<{
  initialTab: TabId;
}>();

const emit = defineEmits<{
  (e: "back-to-home"): void;
}>();

const activeTab = ref<TabId>(props.initialTab || "oke");

watch(
  () => props.initialTab,
  (v) => {
    if (v) activeTab.value = v;
  }
);

const tabs: { id: TabId; label: string }[] = [
  { id: "oke", label: "OKE – NFT & TBA" },
  { id: "communications", label: "Communication" },
  { id: "map", label: "AI Map & Glocal" },
  { id: "finance", label: "ART Token Finance" },
  { id: "activation", label: "Activation 360°" }
];
</script>

<template>
  <div class="min-h-screen bg-gray-50 text-gray-900">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-6 space-y-6">
      <div class="flex items-center justify-between gap-4">
        <div>
          <h1 class="text-2xl font-extrabold tracking-tight">AMAS Dashboard</h1>
          <p class="text-xs text-gray-600">
            OKE・Communication・AI Map・Finance・Activation 360°
          </p>
        </div>
        <button
          class="text-xs px-3 py-1.5 rounded-full border border-gray-300 text-gray-600 hover:bg-gray-100"
          @click="emit('back-to-home')"
        >
          AMAS Home
        </button>
      </div>

      <!-- タブ -->
      <div class="flex gap-2 overflow-x-auto border-b border-gray-200 pb-1 text-sm bg-white rounded-t-xl">
        <button
          v-for="tab in tabs"
          :key="tab.id"
          @click="activeTab = tab.id"
          :class="[
            'px-4 py-2 rounded-t-lg border-b-2',
            activeTab === tab.id
              ? 'border-gray-900 text-gray-900 bg-gray-50'
              : 'border-transparent text-gray-500 hover:text-gray-900 hover:bg-gray-50'
          ]"
        >
          {{ tab.label }}
        </button>
      </div>

      <!-- コンテンツ -->
      <div class="bg-white border border-gray-200 rounded-b-xl p-6 space-y-6">
        <OkeModule v-if="activeTab === 'oke'" />
        <CommModule v-else-if="activeTab === 'communications'" />
        <AiMapModule v-else-if="activeTab === 'map'" />
        <FinanceModule v-else-if="activeTab === 'finance'" />
        <ActivationModule v-else-if="activeTab === 'activation'" />
      </div>
    </div>
  </div>
</template>
