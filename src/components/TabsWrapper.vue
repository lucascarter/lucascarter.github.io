<template>
    <div class="tabs">
        <ul class="main_tab">
            <li :key="mainTabTitle" @click="selectedTitle = mainTabTitle"> {{ mainTabTitle }}</li>
        </ul>
        <ul class="tabs_header">
            <li
                v-for="title in tabTitles"
                :key="title"
                @click="selectedTitle = title"
            >
                {{ title }}
            </li>
        </ul>
        <slot />
    </div>
</template>

<script>
import { ref, provide } from 'vue';
export default {
    setup (props, { slots }) {
        const tabTitles = ref(slots.default().map((tab) => tab.props.title));
        const mainTabTitle = ref(tabTitles.value.shift());
        let selectedTitle = ref(mainTabTitle.value);
        provide("selectedTitle", selectedTitle);
        return {
            selectedTitle,
            tabTitles,
            mainTabTitle
        }
    }

}
</script>

<style scoped>
.tabs {
    margin: 0 auto;
}
.tabs_header, .main_tab {
    margin-bottom: 10px;
    list-style: none;
    padding: 0;
    display: block;
    align-content: center;

}

.main_tab {
    display: block;
}

li {
    text-align: center;
    padding: 10px 20px;
    margin-right: 10px;
    cursor: pointer;
    display: inline;
}

</style>