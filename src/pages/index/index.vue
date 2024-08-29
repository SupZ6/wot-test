<template>
  <view class="wrap">
    <wd-notice-bar :text="textArray1" @next="onNext1" />
    <wd-gap />
    <wd-notice-bar :text="textArray2" @next="onNext2" />
    <wd-gap />
    <wd-notice-bar :text="textArray3" />
  </view>
</template>

<script setup>
import { ref } from 'vue';

const textArray1 = ref([
  '用 ref 动态插入数据的 NoticeBar 通知栏补齐',
  ''
]);

const textArray2 = [
  '没有用 ref 动态插入数据的 NoticeBar 通知栏',
  ''
];

const textArray3 = ref([
  '静态数据的 NoticeBar 通知栏补齐补齐补齐补',
  '2024-08-29T11:56:09.398Z'
]);

const onNext1 = () => {
  const now = new Date();
  textArray1.value[1] = now.toISOString();
};

const onNext2 = () => {
  const now = new Date();
  textArray2[1] = now.toISOString();
};
</script>

<style lang="scss">
.wrap {
  padding: 60rpx;
}
</style>