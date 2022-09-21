<template>
    <div>
        <h2>{{state.fname}} {{state.lname}}</h2>
    </div>
</template>

<script>
    import { reactive } from 'vue';
    export default {
        name: 'DemoTwoComponent',
        setup(){
           const state = reactive({
            fname: 'Hiksert',
            lname: 'Iver',
           }) 
           setTimeout(() => {
            state.fname = 'Ragnar',
            state.lname = 'Loth'
           }, 3000);

           return{
            state
           }
        }
    }
</script>

<style scoped>

</style>