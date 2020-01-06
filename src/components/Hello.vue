<template>
  <view>
    <text class="text-color-primary">{{message}}</text>
    <button :title="btnText" :on-press="handleClick"></button>
  </view>
</template>

<script>
export default {
  data() {
    return {
      message: "Welcome!",
      btnText: "Click",
      counter: 0
    };
  },
  methods: {
    handleClick() {
      this.counter++
      alert(`Click x ${this.counter}`)
    }
  }
};
</script>

<style scoped>
.text-color-primary {
  color: blue;
}
</style>