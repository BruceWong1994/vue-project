<template>
    <SlotDemo>
        <!-- {{ msg }} -->
        <template #header="slotProps">
            <p>header------{{ slotProps.txt }}</p>
        </template>
        <template #main>
            <p>main</p>
        </template>
        <template #content>
            content:{{ msg }}
        </template>
    </SlotDemo>
</template>

<script>
    import SlotDemo from './SlotDemo.vue'
    export default {
        data(){
            return{
                msg:'乱写一通舒服哈回电话覅好'
            }
        },
        components:{
            SlotDemo
        }
    }
</script>

<style>

</style>