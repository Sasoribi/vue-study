<template>
<li :class="{'removed' : item.checked } ">
    <div>
        <label>
            <input type="checkbox" :checked="item.checked" v-model="item.checked" />
            {{ item.text }}
        </label>
    </div>
</li>
</template>

<script>
export default {
    name: 'ItemComponent',
    props: ['item'],
    methods: {

    },

}
</script>

<style scoped>
.removed {
    color: gray;
}

.removed span {
    text-decoration: line-through;
}

li {
    list-style-type: none;
}

li span {
    margin-left: 5px;
}
</style>
