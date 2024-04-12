<template>
    <div>
        <p>1111111这是个父组件</p>
        <p>给子组件传个东西：<input type="text" v-model="sendChildTxt"></p>
        <p>这是儿子给我的：{{ getChildTxt }}</p>
        <Child :toChild='sendChildTxt' @toParent="getChild"/>
    </div>
</template>

<script>
    import Child from './c1.vue'
    export default{
        data(){
            return{
                sendChildTxt:'',
                getChildTxt:''
            }
        },
        components:{
            Child
        },
        methods:{
            getChild(data){
                // console.log(data)
                this.getChildTxt = data;
            }
        }
    }
</script>

<style scoped>
div{
    border:1px solid red;
    padding:50px 0;
}
</style>