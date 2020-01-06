<template>
  <view  class="container">
    <HomeScreen v-if="activeScreen === 'Home'" />
    <Screen1 v-if="activeScreen === 'Screen1'" />
    <button title="To Screen 1" :on-press="() => {navigate('Screen1')}" />
  </view>
</template>

<script>
import HomeScreen from "./src/screens/HomeScreen";
import Screen1 from "./src/screens/Screen1";

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