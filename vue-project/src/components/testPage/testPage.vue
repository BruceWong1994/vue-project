<template>
    <div>
        <h4>测试页面</h4>
        <p>
            Ask a yes/no question:
            <input v-model="question" :disabled="loading" />
        </p>
        <p>{{ answer }}</p>
        <div>
            <div class="ns">1</div>
            <div class="ns">2</div>
            <div class="ns">3</div>
            <div class="ns">4</div>
        </div>
    </div>
</template>

<script setup>
    import { ref, watch } from 'vue'

    //async函数
    const question = ref('')
    const answer = ref('Questions usually contain a question mark. ;-)')
    const loading = ref(false)

    watch(question, async (newQuestion, oldQuestion) => {
    if (newQuestion.includes('?')) {
        loading.value = true
        answer.value = 'Thinking...'
        try {
        const res = await fetch('https://yesno.wtf/api')
        answer.value = (await res.json()).answer
        } catch (error) {
        answer.value = 'Error! Could not reach the API. ' + error
        } finally {
        loading.value = false
        }
    }
    })


    //试一试set
    // const set = new Set(document.querySelectorAll('div'));
    // console.log(set);
    // console.log(set.size);
    // console.log(typeof set);
    const arr1 = [2,5,6,8,5,3,1,2];
    const arr2 = [...new Set(arr1)];
    console.log(arr1);
    
    console.log(arr2);
    
    
    

</script>

<style>
    
</style>