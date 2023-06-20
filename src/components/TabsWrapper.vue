<template>
    <div class="tabs">
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
        const selectedTitle = ref(tabTitles.value[0]);
        provide("selectedTitle", selectedTitle)
        return {
            selectedTitle,
            tabTitles

        }
    }

}
</script>

<style scoped>
.tabs {
    margin: 0 auto;
}
.tabs_header{
    margin-bottom: 10px;
    list-style: none;
    padding: 0;
    display: flex;
}

.tabs_header li {
    text-align: center;
    padding: 10px 20px;
    margin-right: 10px;
    cursor: pointer;
}

.tabs_header li #main_title {
    font-size: 300px;
}


</style>