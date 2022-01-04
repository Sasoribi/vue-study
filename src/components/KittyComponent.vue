<template>
<div>
   <span>kitty</span>

        <div><button type="button" @click="fade">Change!</button></div>
</div>
</template>

<script>
export default {
    props:['kitty'],
    methods:{
        fade:function(){
            this.$emit('fade')
        }
    }
};
</script>

<style scoped>

</style>
