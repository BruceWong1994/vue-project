<template>
    <p><input type="text" v-model="msg"></p>
    <div>后面写个啥呢：{{ msg }}</div>
    <SeCom />
</template>

<script>
    import SeCom from './SecondComponents.vue'

    export default {
        data(){
            return{
                msg:''
            }
        },
        components:{
            SeCom
        }
    }
</script>