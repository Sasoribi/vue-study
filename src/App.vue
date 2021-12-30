<template>
<div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <AddItemComponent @add-new-item="addItem"></AddItemComponent>
    <ItemsComponent :items="items"></ItemsComponent>
    <ChangeTitleComponent :msg="msg"></ChangeTitleComponent>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import ItemsComponent from './components/ItemsComponent.vue'
import ChangeTitleComponent from './components/ChangeTitleComponent.vue'
import AddItemComponent from './components/AddItemComponent.vue'

export default {
    name: 'App',
    components: {
        HelloWorld,
        ItemsComponent,
        ChangeTitleComponent,
        AddItemComponent,
    },
    data() {
        return {
            items: [{
                    text: 'Bananas',
                    checked: true
                },
                {
                    text: 'Apples',
                    checked: false
                }
            ],
            newItem: '',
            msg: 'Title'
        }
    },
    methods: {
        addItem: function (itemValue) {
            if (itemValue) {
                itemValue = itemValue.trim()
                this.items.push({
                    text: itemValue,
                    checked: false
                });
            }

        }
    }
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
