<template>
    <div class="header">
      <tabs-wrapper>
        <my-tab title="lucas carter" id="main_title"><home-page></home-page></my-tab>
        <my-tab title="resume"><resume-page></resume-page></my-tab>
        <my-tab title="code"><code-page></code-page></my-tab>
        <my-tab title="photos"><photos-page></photos-page></my-tab>
        <my-tab title="travel"><travel-page></travel-page></my-tab>
      </tabs-wrapper>
    </div>
</template>

<script>
import MyTab from './components/MyTab.vue';
import TabsWrapper from './components/TabsWrapper.vue';
import HomePage from './components/HomePage.vue';
import ResumePage from './components/ResumePage.vue';
import CodePage from './components/CodePage.vue';
import PhotosPage from './components/PhotosPage.vue';
import TravelPage from './components/TravelPage.vue';

export default {
  name: 'App',
  components: {
    MyTab,
    TabsWrapper,
    HomePage,
    ResumePage,
    CodePage,
    PhotosPage,
    TravelPage
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;1,100;1,200;1,300;1,400;1,500;1,600;1,700&display=swap');

#app {
  text-align: center;
  margin-top: 1em;
  font-family: 'Montserrat', sans-serif;
}
p {
  text-align: left;
}

</style>
