<template>
    <div class="outer">
        <h4>组合式API：Class 与 Style 绑定</h4>
        <!-- <div class="static" :class='{active:isActive,textDanger:isDanger}'>{{ a }}</div> -->
        <div class="names" :class= classObject >this is a test text</div>
        <button @click="changeColor">换个颜色</button>
    </div>
</template>

<script setup>
    import {ref,reactive,computed} from 'vue';
    // const classObject = reactive({
    //     active:true,
    //     textDanger:false
    // })
    // const changeColor = ()=>{
    //     classObject.active = !classObject.active;
    //     classObject.textDanger = !classObject.textDanger;
    //     console.log(classObject);
    // }

    const isActive = ref(true);
    const isDanger = ref(false);
    // const classObject = reactive({
    //     active:isActive,
    //     textDanger:isDanger
    // })
    const classObject = computed(()=>
        ({
            active: isActive.value,
            textDanger: isDanger.value
        })
    )
    const changeColor = ()=>{
        isActive.value = !isActive.value;
        isDanger.value = !isDanger.value;
        console.log(classObject);
    }
</script>

<style>
    .active{
        background:orange;
    }
    .textDanger{
        color:red;
    }
</style>