<template>
    <div>
        这是A页面
    </div>
</template>
<script>
    export default{
        beforeUnmount(){
            console.log('A卸载前')
        },
        unmounted(){
            console.log('A卸载后')
        }
    }
</script>