<template>
<div>
    <ul>
        <ItemComponent v-for="(item, index) in items" :key="index" :item="item">
        </ItemComponent>
    </ul>
</div>
</template>

<script>
import ItemComponent from './ItemComponent.vue'

export default {
    name: 'ItemsComponent',
    props: ['items'],
    components: {
        ItemComponent
    }
}
</script>

<style scoped>

</style>
