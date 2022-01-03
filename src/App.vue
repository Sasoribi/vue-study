<template>
<div id="app">
    <img src="./assets/logo.png">
    <h2><span>Paramodo</span>
        <control-component></control-component>
    </h2>
    <state-title-compoent></state-title-compoent>
    <count-down-component></count-down-component>
    <kitty-component></kitty-component>
</div>
</template>

<script>
import StateTitleCompoent from './components/StateTitleCompoent.vue'
import ControlComponent from './components/ControlComponent.vue'
import CountDownComponent from './components/CountDownComponent.vue'
import KittyComponent from './components/KittyComponent.vue'

export default {
    name: 'App',
    components: {
        StateTitleCompoent,
        ControlComponent,
        CountDownComponent,
        KittyComponent
    },
    data() {
        return {}
    },
    methods: {}
}
</script>

<style>
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
