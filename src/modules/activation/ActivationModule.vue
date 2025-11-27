<script setup lang="ts">
/**
 * ここに Activation 360° の円形チャネル UI と
 * AP2 ベースの AI 決済フローのトリガーを統合します。
 */
</script>

<template>
  <section class="space-y-6">
    <h2 class="text-xl font-semibold text-gray-900">
      Activation 360°
    </h2>
    <p class="text-sm text-gray-600">
      Newsletter / Instagram / TikTok / Web / In-store / OOH など、
      全チャネルのアクティベーション設計を 360° で可視化するエリア。
    </p>

    <div
      class="relative mx-auto w-64 h-64 rounded-full border border-dashed border-gray-300 flex items-center justify-center text-xs text-gray-500"
    >
      <div class="text-center">
        <div class="text-sm font-semibold mb-1">AMAS</div>
        <div class="text-[11px] text-gray-500">Activation Hub</div>
      </div>

      <div class="absolute -top-3 left-1/2 -translate-x-1/2 text-[10px] text-gray-500">
        Newsletter / Email
      </div>
      <div class="absolute top-1/2 -translate-y-1/2 -left-6 rotate-[-90deg] text-[10px] text-gray-500">
        Instagram / TikTok
      </div>
      <div class="absolute top-1/2 -translate-y-1/2 -right-6 rotate-[90deg] text-[10px] text-gray-500">
        Web / In-store
      </div>
      <div class="absolute -bottom-3 left-1/2 -translate-x-1/2 text-[10px] text-gray-500">
        OOH / Influencers
      </div>
    </div>

    <div class="border border-gray-200 rounded-xl p-4 bg-white space-y-3 text-sm">
      <h3 class="font-semibold">AI-driven Payments（AP2）</h3>
      <p class="text-xs text-gray-600">
        Google の AP2（AI-driven Payments Protocol）と連携し、
        キャンペーン型の支払い・サブスクリプションを AI エージェントに委任するデモをここに実装します。
      </p>
      <button
        class="w-full mt-2 py-2 rounded-lg bg-gray-900 text-white text-sm font-semibold hover:bg-black"
      >
        Start AP2 Payment Flow（デモ）
      </button>
    </div>
  </section>
</template>
