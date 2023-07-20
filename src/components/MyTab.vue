<template>
    <div class="tab-content-wrapper">
            <div class="tab-content" :key="title" v-show="title == selectedTitle">
                <slot />
            </div>
    </div>
</template>

<script>
import { inject } from 'vue';
export default {
    props: ['title'],
    setup(){
        const selectedTitle = inject("selectedTitle");

        return {
            selectedTitle
        }
    }

}
</script>

<style>



.tab-content {
    align-content: center;
    margin: 4em;
    margin-bottom: 10em;
}


.fade-leave-active {
  transition: opacity 0s;
}
.fade-enter-active{
    transition: opacity 2.5s;
    /* transition-delay: 0.4s; */
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.transition {
    position: relative;
}



</style>