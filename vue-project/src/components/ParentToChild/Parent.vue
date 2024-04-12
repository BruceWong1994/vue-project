<template>
    <div>
        <p>这是个父组件</p>
        <p>给子组件传个东西：<input type="text" v-model="sendChildTxt"></p>
        <Child :toChild='sendChildTxt'/>
    </div>
</template>

<script>
import Child from './Child.vue'
    export default{
        data(){
            return{
                sendChildTxt:'',
            }
        },
        components:{
            Child
        },
    }
</script>

<style scoped>
div{
    border:1px solid red;
    padding:50px 0;
}
</style>