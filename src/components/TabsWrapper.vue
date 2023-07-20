<template>
    <div class="tabs">
        <ul class="main_tab">
            <li :key="mainTabTitle" :class="{ selected: selectedTitle == mainTabTitle}" @click="selectedTitle = mainTabTitle" > {{ mainTabTitle }}</li>
        </ul>
        <ul class="tabs_header">
            <li
                v-for="title in tabTitles"
                :key="title"
                :class="{ selected: selectedTitle == title}"
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
.tabs li:hover {
    border-bottom: 1px solid black;
}

.tabs li.selected {
    border-bottom: 1px solid black;
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
    margin-top: 1em;
    margin: 2em;
}
.main_tab li {
    font-size: 5em;
    font-weight: 200;
    letter-spacing: 0.2em;
    padding: 0%;
    padding-bottom: 5px;
    border-bottom: 1px solid transparent;
    transition: 0.4s all ease-out;
}

.tabs_header li {
    font-size: 2em;
    font-weight: 300;
    padding: 0%;
    padding-bottom: 5px;
    margin: 35px;
    margin-right: 1.2em;
    margin-left: 1.2em;
    border-bottom: 1px solid transparent;
    transition: 0.4s all ease-out;
}

li {
    text-align: center;
    padding: 10px 20px;
    margin-right: 0px;
    cursor: pointer;
    display: inline;
}



</style>