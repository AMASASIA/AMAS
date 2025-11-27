<script setup lang="ts">
import MetricCard from "@/components/MetricCard.vue";

/**
 * ここに ART Token 財務 / Wallet 連携 / Stripe 決済 UI を統合します。
 * AIM3-Vue-project の Stripe + NFT Mint フローをベースに実装可能です。
 */
</script>

<template>
  <section class="space-y-6">
    <h2 class="text-xl font-semibold text-gray-900">
      ART Token Finance &amp; Wallet
    </h2>

    <div class="grid md:grid-cols-3 gap-4">
      <MetricCard title="Total Revenue" value="$120,050" change="+6.5%" />
      <MetricCard title="Net Value" value="$18,900" change="+5.2%" />
      <MetricCard title="Portfolio Value" value="$250,000" change="+12.5%" />
    </div>

    <div class="grid md:grid-cols-2 gap-4 text-sm">
      <div class="border border-gray-200 rounded-xl p-4 bg-white space-y-2">
        <h3 class="font-semibold">Wallet / ART Token</h3>
        <p class="text-xs text-gray-600">
          接続されたウォレットの残高と ART Token のポジションを表示します。
        </p>
        <div class="border border-dashed border-gray-300 rounded-lg h-24 flex items-center justify-center text-xs text-gray-500">
          Wallet &amp; Token Positions（プレースホルダー）
        </div>
      </div>
      <div class="border border-gray-200 rounded-xl p-4 bg-white space-y-2">
        <h3 class="font-semibold">Stripe 決済</h3>
        <p class="text-xs text-gray-600">
          Stripe Checkout 完了時に NFT/SBT/TBA をミントするフローをここに統合します。
        </p>
        <button
          class="w-full mt-2 py-2 rounded-lg bg-gray-900 text-white text-sm font-semibold hover:bg-black"
        >
          Stripe Checkout（デモ）
        </button>
      </div>
    </div>
  </section>
</template>
