<template>
    <keep-alive>
        <component :is="currentTab"></component>
    </keep-alive>
    
    <!-- <TabA />
    <TabB /> -->
    <p><button @click="changeHandle">点击切换tab</button></p>
</template>
<script>
    import TabA from './TabA.vue';
    import TabB from './TabB.vue';
    export default{
        data(){
            return {
                currentTab:'TabA'
            }
        },
        components:{
            TabA,
            TabB
        },
        methods:{
            changeHandle(){
                this.currentTab = this.currentTab == 'TabA'? 'TabB': 'TabA';
                console.log(this.currentTab);
            }
        }
    }
</script>