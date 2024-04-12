<template>
    <div>
        <h3>子组件</h3>
        <p>给父组件传点什么呢: <input type="text" v-model="msg"></p>
        <button @click="sendToParent">传下试试</button>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                msg:''
            }
        },
        methods:{
            sendToParent(){
                this.$emit('toParent',this.msg)
            }
        }
    }
</script>

<style scoped>
    div{
        border:1px solid green;
    }
</style>