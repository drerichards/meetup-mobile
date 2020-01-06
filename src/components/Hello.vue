<template>
  <view>
    <text class="text-color-primary content">{{message}}</text>
    <button :title="btnText" :on-press="handleClick"></button>
    <text class="content">{{counter}}</text>
    <text>{{clickMessage}}</text>
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
  computed: {
    clickMessage() {
      if (this.counter > 0 && this.counter < 6) {
        return 'Just a little more...'
      } else if (this.counter > 5) {
        return 'Good! Keep Clicking!'
      }
      return 'Nothing Clicked...'
    }
  },
  methods: {
    handleClick() {
      this.counter++
    }
  }
};
</script>

<style scoped>
.content {
  text-align: center;
}
.text-color-primary {
  color: blue;
}
</style>