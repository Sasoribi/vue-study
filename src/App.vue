<template>
<div id="app">
    <img src="./assets/logo.png">
    <h2><span>Paramodo</span>
        <control-component></control-component>
    </h2>
    <state-title-compoent></state-title-compoent>
    <count-down-component></count-down-component>
        <transition name="fade">
        <kitty-component v-if="kitty" @fade="fade" :kitty="kitty"></kitty-component>
    </transition>

</div>
</template>

<script>
import StateTitleCompoent from './components/StateTitleCompoent.vue'
import ControlComponent from './components/ControlComponent.vue'
import CountDownComponent from './components/CountDownComponent.vue'
import KittyComponent from './components/KittyComponent.vue'

window.data = {
    kitty: true
}
export default {
    name: 'App',
    components: {
        StateTitleCompoent,
        ControlComponent,
        CountDownComponent,
        KittyComponent
    },
    data() {
        return window.data
    },
    methods: {
        fade:function(){
            this.kitty = !this.kitty
        }
    }
}
</script>

<style scoped>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
.fade-enter-active,
.fade-leave-active {
    transition: opacity .5s
}

.fade-enter,
.fade-leave-active {
    opacity: 0
}
</style>
