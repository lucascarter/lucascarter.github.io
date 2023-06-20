<template>
    <div class="header">
        <tabs-wrapper>
            <my-tab title="lucas carter" id="main_title">MY HOME PAGE</my-tab>
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

export default {
  name: 'App',
  components: {
    MyTab,
    TabsWrapper,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
