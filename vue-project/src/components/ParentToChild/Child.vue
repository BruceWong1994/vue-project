<template>
    <div>
        <p>这是个子组件</p>
        <p>拿到了：{{ toChild }}</p>
    </div>
</template>

<script>
    export default {
        props:['toChild']
    }
</script>

<style scoped>
div{
    border:1px solid blue;
}
</style>