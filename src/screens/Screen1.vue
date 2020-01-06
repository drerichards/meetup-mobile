<template>
  <view>
    <text class="text-color-primary">{{title}}</text>
    <button title="To Home" :on-press="() => {navigate('Home')}" />
  </view>
</template>

<script>
export default {
  props: {
    navigate: {
      type: Function
    }
  },
  data() {
    return { title: "Screen 1" };
  }
};
</script>

<style>
.text-color-primary {
  color: blue;
}
</style>
