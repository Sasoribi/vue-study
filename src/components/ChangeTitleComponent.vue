<template>
<div>
    <span class="font-bold">Title:</span><input type="text" v:model="msg" @change="change">
</div>
</template>

<script>
export default {
    props: ['msg'],
    methods: {
        change:function(){
            console.log(this.msg);
        }
    },
}
</script>

<style scoped>
.font-bold {
    font-weight: bold
}
</style>
