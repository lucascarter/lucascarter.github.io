<template>
    <div class="tabs">
        <ul class="main_tab">
            <li :key="mainTabTitle" :class="{ selected: selectedTitle == mainTabTitle}" @click="selectedTitle = mainTabTitle" > {{ mainTabTitle }}</li>
        </ul>
        <div id="nav-icon" v-on:click="toggleNavMenu">
            <span></span>
            <span></span>
            <span></span>
        </div>
        <ul id="nav-menu" :class="{ 'show-on-mobile': isNavMenuVisible, 'hide-on-mobile': !isNavMenuVisible }">
            <ul class="tabs_header">
            <li
                v-for="title in tabTitles"
                :key="title"
                :class="{ selected: selectedTitle == title}"
                @click="selectedTitle = title; toggleNavMenu()"
                >
                {{ title }}
            </li>
        </ul>
        </ul>

        <slot />
    </div>
</template>

<script>
import { ref, provide } from 'vue';
export default {
    data() {
        return {
            isNavMenuVisible: false,
            isMobile: window.innerWidth <= 768
        };
    },
    methods: {
        toggleNavMenu() {
            this.isNavMenuVisible = !this.isNavMenuVisible;
        },
        checkIfMobile() {
            this.isMobile = window.innerWidth <= 768;
        }
    },
    created() {
        window.addEventListener('resize', this.checkIfMobile);
    },
    unmounted() {
        window.removeEventListener('resize', this.checkIfMobile);
    },
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
    max-width: 100%;
    overflow-wrap: break-word;
    word-wrap: break-word; /* Break the word at the end of the line */
    word-break: break-word; /* Break the word at the end of the line */

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
#nav-icon {
    cursor: pointer;
    display: none;
}

#nav-icon span {
    display: block;
    width: 33px;
    height: 2px;
    margin-bottom: 5px;
    margin-top: 5px;
    background: #000;
}

#nav-menu {
    list-style-type: none;
    padding: 0;
}
#nav-menu li:first-child {
    margin-top: 0;
}

.hide-on-mobile {
    display: none;
}
/* Media query for mobile devices */
@media (max-width: 768px) {
    .tabs {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .main_tab li {
        font-size: 3em; /* Adjust font size */
        align-content: center;
    }
    .tabs_header li {
        font-size: 2em;
    }

    li {
        padding: 5px 10px; /* Adjust padding */
        display: block;
    }

    .main_tab, .tabs_header {
        margin: 1em; /* Adjust margin */
    }
    #nav-icon {
        display: block;
    }
    #nav-menu.hide-on-mobile {
        display: none;
    }
    #nav-menu.show-on-mobile {
        display: block;
    }
}


</style>