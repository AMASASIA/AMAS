<script setup lang="ts">
import { ref } from "vue";

/**
 * ここに oke-alt-demo-vite-app から AtomicMint や
 * Token Bound Account 関連のコンポーネント／ロジックを組み込みます。
 *
 * 例：
 * import AtomicMint from "./AtomicMint.vue";
 * import OkeTbaPanel from "./OkeTbaPanel.vue";
 */
const walletAddress = ref("");
const cardName = ref("");
const imageUrl = ref("");
</script>

<template>
  <section class="space-y-6">
    <h2 class="text-xl font-semibold">
      OKE — NFT Generator &amp; Token Bound Account
    </h2>

    <div class="grid md:grid-cols-2 gap-6">
      <!-- 左：NFT Generator デモ -->
      <div class="border border-gray-200 rounded-xl p-4 bg-white space-y-3 text-sm">
        <h3 class="font-semibold text-gray-900">NFT Generator</h3>
        <input
          v-model="cardName"
          class="w-full border border-gray-300 rounded-lg px-3 py-2"
          placeholder="OKE / NFT 名"
        />
        <input
          v-model="imageUrl"
          class="w-full border border-gray-300 rounded-lg px-3 py-2"
          placeholder="画像URL / IPFS"
        />
        <input
          v-model="walletAddress"
          class="w-full border border-gray-300 rounded-lg px-3 py-2"
          placeholder="ウォレットアドレス"
        />
        <button
          class="w-full mt-2 py-2 rounded-lg bg-gray-900 text-white text-sm font-semibold hover:bg-black"
        >
          Mint OKE NFT（デモ）
        </button>

        <p class="text-xs text-gray-500">
          実際の AtomicMint コンポーネントに差し替える想定です。
        </p>
      </div>

      <!-- 右：Token Bound Account 情報エリア -->
      <div class="border border-gray-200 rounded-xl p-4 bg-white space-y-3 text-sm">
        <h3 class="font-semibold text-gray-900">Token Bound Account</h3>
        <p class="text-xs text-gray-600">
          ここに TBA のアドレス / 残高 / トランザクション などを表示します。
          実装時には oke-alt-demo-vite-app の TBA ロジックを組み込みます。
        </p>
        <div
          class="border border-dashed border-gray-300 rounded-lg h-32 flex items-center justify-center text-xs text-gray-500"
        >
          TBA Info / Balance / Actions（プレースホルダー）
        </div>
      </div>
    </div>
  </section>
</template>
