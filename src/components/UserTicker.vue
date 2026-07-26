<template>
  <div class="glass-card ticker-card">
    <div class="ticker-wrapper">
      <div v-for="(item, index) in tickerItems" :key="index" class="ticker-item">
        <span>{{ item.text }}</span>
        <span style="color: var(--success-color); font-weight: bold;">[生成完成]</span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const tickerItems = ref([
  {
    "text": "用户 139****7711 完成了 7 个月宝宝高铁高锌辅食食谱设计"
  },
  {
    "text": "用户 186****2209 生成了新生儿肠胀气飞机抱与排气操指南"
  },
  {
    "text": "用户 131****5588 完成了 1 岁半幼儿语言黄金期互动训练方法"
  },
  {
    "text": "用户 158****9920 生成了产后顺产 4 周阶段性月子食谱"
  },
  {
    "text": "用户 173****4411 取得了自主入睡吃玩睡作息建立表"
  }
]);
</script>
