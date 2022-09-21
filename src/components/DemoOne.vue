<template>
    <div>
        <h4>{{name}}</h4>
    </div>
</template>

<script>
    import {ref} from 'vue'
    export default {
        name: 'DemoOneComponent',
        setup(){
            const name = ref('Nauman khan')
            setTimeout(() => {
                name.value ='codeVolution'
            }, 2000);
            return{
                name,
            }
        
        }
    }
</script>

<style scoped>

</style>