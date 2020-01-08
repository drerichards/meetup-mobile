<template>
  <view class="container">
    <HomeScreen v-if="activeScreen === 'Home'" :navigate="navigate" />
    <Screen1 v-if="activeScreen === 'Screen1'" :navigate="navigate" />
  </view>
</template>

<script>
import HomeScreen from "@/screens/HomeScreen";
import Screen1 from "@/screens/Screen1";

export default {
  components: {
    HomeScreen,
    Screen1
  },
  data() {
    return { activeScreen: "Home" };
  },
  methods: {
    navigate(screen) {
      this.activeScreen = screen;
    }
  }
};
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
</style>