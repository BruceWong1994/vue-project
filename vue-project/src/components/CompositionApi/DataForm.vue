<template>
    <div>
        <h4>输入绑定</h4>

        <h5>单选框：</h5>
        <p>我的性别：{{ picked }}</p>
        <input type="radio" id="male" value="male" v-model="picked" />
        <label for="male">男</label>
        <input type="radio" id="female" value="female" v-model="picked" />
        <label for="female">女</label>

        <h5>复选框：</h5>
        <p>我有哪几只猫：{{ mycats.length>0? mycats: '一只也没有' }}</p>
        <input type="checkbox" id="bai" value="小白"  v-model="mycats">
        <label for="bai">小白</label>
        <input type="checkbox" id="hua" value="小花"  v-model="mycats">
        <label for="hua">小花</label>
        <input type="checkbox" id="mi" value="糯米"  v-model="mycats">
        <label for="mi">糯米</label>

        <h5>选择器：</h5>
        <p>我更喜欢哪只猫：{{ perfer=='bai'?'小白':perfer == 'hua'?'小花':perfer=='mi'?'糯米':'还没选呢' }}</p>
        <select v-model="perfer">
            <option value="" disabled>请选择</option>
            <option value="bai">小白</option>
            <option value="hua">小花</option>
            <option value="mi">糯米</option>
        </select>

        <p>测试一下：{{ ss }}</p>
        <select v-model="ss">
            <option value="" disabled>请选择</option>
            <option :value="op.value" v-for="op of options">{{ op.text }}</option>
        </select>

        <p>看看：{{ as }}</p>
        <select v-model="as">
            <option :value="{ number: 123 }">aaa</option>
        </select>

        <!-- <input
            type="checkbox"
            v-model="toggle"
            true-value="yes"
            false-value="no" 
        /> -->
    </div>
</template>

<script setup>
    import {reactive, ref} from 'vue';

    let picked = ref('male'), perfer = ref(''), ss=ref(''), as=ref('');
    const mycats = ref([]);
    const options = ref([
        { text: 'One', value: 'A' },
        { text: 'Two', value: 'B' },
        { text: 'Three', value: 'C' }
    ])
</script>

<style>
    
</style>