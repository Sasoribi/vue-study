<template>
<div>
    <div class="input-group">
        <input type="text" class="input form-control" placeholder="Please Input Item Name..." v-model="itemValue">
        <span class="input-group-btn">
            <button class="btn btn-default" type="button" @click="addNewItem">AddItem</button>
        </span>
    </div>
</div>
</template>

<script>
export default {
    data: function () {
        return {
            itemValue: ''
        }
    },
    methods: {
        addNewItem: function () {
            const newItem = this.itemValue
            this.$emit('add-new-item', newItem)
            this.itemValue = ""
        }
    }
}
</script>

<style scoped>

</style>
