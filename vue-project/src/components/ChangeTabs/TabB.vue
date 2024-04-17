<template>
    <div>
        这是B页面
    </div>
</template>
<script>
    export default{
        beforeUnmount(){
            console.log('B卸载前')
        },
        unmounted(){
            console.log('B卸载后')
        }
    }
</script>