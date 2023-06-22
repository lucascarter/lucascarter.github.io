<template>
    <div class="header">
      <tabs-wrapper>
        <my-tab title="lucas carter" id="main_title"><home-page></home-page></my-tab>
        <my-tab title="cv">MY RESUME</my-tab>
        <my-tab title="code">MY PROJECTS</my-tab>
        <my-tab title="photos">FILM PHOTOS</my-tab>
        <my-tab title="travel">MY TRAVEL CONTENT</my-tab>
      </tabs-wrapper>
    </div>
</template>

<script>
import MyTab from './components/MyTab.vue';
import TabsWrapper from './components/TabsWrapper.vue';
import HomePage from './components/HomePage.vue';

export default {
  name: 'App',
  components: {
    MyTab,
    TabsWrapper,
    HomePage
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap');

#app {

  text-align: center;
  margin-top: 60px;
  font-family: 'Montserrat', sans-serif;
}
</style>
