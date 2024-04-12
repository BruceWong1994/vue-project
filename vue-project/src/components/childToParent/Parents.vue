<template>
    <div>
        <h3>父组件</h3>
        <p>看看子组件给我传了什么: <span>{{ receive }}</span></p>
        <Children @toParent="getChild" />
    </div>
</template>

<script>
    import Children from './Children.vue';
    export default {
        components:{
            Children
        },
        data(){
            return {
                receive:''
            }
        },
        methods:{
            getChild(data){
                this.receive = data
            }
        }
    }
</script>

<style scoped>
    div{
        border:1px solid red;
        padding:50px 10px;
    }
</style>