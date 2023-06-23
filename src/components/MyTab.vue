<template>
    <div class="alignment-wrapper">
        <transition name="fade">
            <div class="tab-content" :key="title" v-show="title == selectedTitle">
                <slot />
            </div>
        </transition>
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
    padding: 200px;
    border: 5px solid black;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}


.fade-leave-active {
  transition: opacity 0.4s;
}
.fade-enter-active{
    transition: opacity 2.5s;
    transition-delay: 0.4s;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.transition {
    position: relative;
}



</style>