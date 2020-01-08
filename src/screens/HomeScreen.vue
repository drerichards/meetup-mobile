<template>
  <view>
    <text class="text-color-primary">{{title}}</text>
    <Hello />
    <button title="To Screen 1" :on-press="() => {navigate('Screen1')}" />
  </view>
</template>

<script>
import Hello from "../components/Hello";

export default {
  props: {
    navigate: {
      type: Function
    }
  },
  components: {
    Hello
  },
  data() {
    return { title: "My app" };
  }
};
</script>

<style>
.text-color-primary {
  text-align: center;
  color: blue;
}
</style>
