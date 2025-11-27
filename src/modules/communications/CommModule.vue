<script setup lang="ts">
/**
 * ここに AIM3-Vue-project / AIM3-ADM-WAKU から
 * Messaging / Chat Rooms / Video Chat の UI を統合します。
 */
</script>

<template>
  <section class="space-y-4">
    <h2 class="text-xl font-semibold text-gray-900">
      Communication Hub
    </h2>
    <p class="text-sm text-gray-600">
      Real-time Messaging / Waku / Chat Rooms / Video Chat の統合デモエリアです。
    </p>

    <div class="grid md:grid-cols-3 gap-4 text-sm">
      <div class="border border-gray-200 rounded-xl p-4 bg-white">
        <h3 class="font-semibold mb-2">Messaging</h3>
        <p class="text-xs text-gray-600">
          Waku ベースの分散メッセージング UI をここに配置します。
        </p>
      </div>
      <div class="border border-gray-200 rounded-xl p-4 bg-white">
        <h3 class="font-semibold mb-2">Chat Rooms</h3>
        <p class="text-xs text-gray-600">
          General / NFT Trading / Web3 Dev などのルーム一覧とメンバー数。
        </p>
      </div>
      <div class="border border-gray-200 rounded-xl p-4 bg-white">
        <h3 class="font-semibold mb-2">Video Chat</h3>
        <p class="text-xs text-gray-600">
          WebRTC / LiveKit ベースのビデオチャットをここに組み込みます。
        </p>
      </div>
    </div>
  </section>
</template>
