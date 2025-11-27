<script setup lang="ts">
type TabId = "oke" | "communications" | "map" | "finance" | "activation";

const emit = defineEmits<{
  (e: "select-tab", tab: TabId): void;
}>();

function onVoiceTap() {
  // 将来的に音声入力処理をここに実装
  emit("select-tab", "activation");
}
</script>

<template>
  <div class="flex flex-col items-center justify-center min-h-screen text-gray-100">
    <h1 class="text-4xl md:text-5xl font-extrabold tracking-wide mb-10">
      AMAS
    </h1>

    <!-- 中央 AI Hub -->
    <button
      class="w-44 h-44 md:w-52 md:h-52 rounded-full bg-gradient-to-br from-gray-900 to-black
             border border-gray-700 flex flex-col items-center justify-center shadow-[0_0_80px_rgba(255,255,255,0.14)] mb-10"
      @click="onVoiceTap"
    >
      <!-- ここに逆▼風アレンジの音声アイコン画像を配置（public/voice-icon.svg など） -->
      <div class="flex items-end gap-1 mb-3">
        <span class="w-1.5 h-6 bg-gray-300 rounded-full"></span>
        <span class="w-1.5 h-9 bg-gray-500 rounded-full"></span>
        <span class="w-1.5 h-12 bg-gray-200 rounded-full"></span>
        <span class="w-1.5 h-9 bg-gray-500 rounded-full"></span>
        <span class="w-1.5 h-6 bg-gray-300 rounded-full"></span>
      </div>
      <p class="text-xs uppercase tracking-wide text-gray-400">
        AI Hub
      </p>
    </button>

    <!-- 下 6 ボタン -->
    <div class="grid grid-cols-2 gap-4 w-80 max-w-xs text-sm">
      <button class="hub-btn" @click="emit('select-tab','communications')">
        Messaging
      </button>
      <button class="hub-btn" @click="emit('select-tab','communications')">
        Chat Rooms
      </button>
      <button class="hub-btn" @click="emit('select-tab','communications')">
        Video Chat
      </button>
      <button class="hub-btn" @click="emit('select-tab','map')">
        AI Map
      </button>
      <button class="hub-btn" @click="emit('select-tab','oke')">
        OKE
      </button>
      <button class="hub-btn" @click="emit('select-tab','activation')">
        Activation 360°
      </button>
    </div>
  </div>
</template>

<style scoped>
.hub-btn {
  width: 100%;
  padding: 0.85rem 1rem;
  border-radius: 0.9rem;
  background: #202020;
  border: 1px solid #383838;
  color: #f5f5f5;
  transition: background 0.15s ease, transform 0.1s ease, box-shadow 0.1s ease;
}
.hub-btn:hover {
  background: #2a2a2a;
  box-shadow: 0 0 16px rgba(255, 255, 255, 0.08);
  transform: translateY(-1px);
}
</style>
