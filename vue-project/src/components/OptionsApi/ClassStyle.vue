<template>
    <div class="outer">
        <h4>选项式API：Class 与 Style 绑定</h4>
        <!-- <div class="static" :class='{active:isActive,textDanger:isDanger}'>{{ a }}</div> -->
        <div class="names" :class= classObject >this is a test text</div>
        <button @click="changeColor">换个颜色</button>
    </div>
</template>

<script>
    export default{
        data(){
           return{
            // isActive: true,
            // isDanger: false,
            // classObject: {
            //     active: this.isActive,
            //     textDanger: this.isDanger
            // }
            classObject:{
                active:true,
                textDanger:false
            }
           }
        },
        // computed:{
        //     classObject(){
        //         return {
        //             active:this.isActive,
        //             textDanger:this.isDanger
        //         }
        //     }
        // },
        methods:{
            // changeColor(){
            //     console.log('get in');
            //     // this.classObject.active= false
            //     // this.classObject.textDanger = true

            //     this.isActive = false
            //     this.isDanger = true
            //     console.log(this.classObject);
            // }
            changeColor(){
                console.log('get in');
                // this.classObject.active= false
                // this.classObject.textDanger = true
                this.classObject={active:!this.classObject.active,textDanger:!this.classObject.textDanger}
                console.log(this.classObject);
            }
        }
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