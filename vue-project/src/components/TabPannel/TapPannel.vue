<template>
    <div class="aside">

    </div>
    <div class="maincontent">
        <!-- <ComputedPage />
        <ClassStyle1 />
        <ClassStyle2 />
        <VFor />
        <DataForm /> -->

        <testPage />
    </div>
</template>

<script setup>
    import testPage from '../testPage/testPage.vue';

    import ComputedPage from '../CompositionApi/ComputedPage.vue';

    import ClassStyle1 from '../CompositionApi/ClassStyle.vue';
    import ClassStyle2 from '../OptionsApi/ClassStyle.vue';

    import VFor from '../CompositionApi/VForPage.vue';

    import DataForm from '../CompositionApi/DataForm.vue';
</script>

<style>
    .aside{
        position: fixed;
        left: 0px;
        top: 100px;
        width: 150px;
        height: 400px;
        border: 1px solid red;
        background:purple;
    }
    .maincontent{
        margin-left:150px;
        /* background:#ccc; */
        max-width:100%;
        border:1px solid green;
    }
</style>