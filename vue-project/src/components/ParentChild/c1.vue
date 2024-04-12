<template>
    <div>
        <p>222222这是个子组件</p>
        <p>拿到了：{{ toChild }}</p>
        <p><input type="text" v-model="toFatherMsg" @keyup="toFather"></p>
    </div>
</template>

<script>
    export default {
        props:['toChild'],
        data(){
            return{
                toFatherMsg:''
            }
        },
        methods:{
            toFather(){
                // console.log('进来了？');
                this.$emit('toParent',this.toFatherMsg)
            }
        }
    }
</script>

<style scoped>
div{
    border:1px solid blue;
}
</style>