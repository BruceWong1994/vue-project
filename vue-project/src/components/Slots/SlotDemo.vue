<template>
    <slot name="header" :txt="msg"></slot>
    <slot name="main"></slot>
    <slot name="content"></slot>
</template>

<script>
    export default {
        data(){
            return{
                msg:'这是给父组件的'
            }
        }
    }
</script>

<style>
</style>