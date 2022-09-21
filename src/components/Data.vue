<template>
    <div>
      <h4>Options - {{c_fname}}</h4>
    <h4>Composition -{{o_fname}}</h4>
    <h4>Composition - {{greet}}</h4>
    </div>
</template>

<script>
    import {ref} from 'vue'
    export default {
        name: 'DataComponent',
        setup(){
            const c_fname = ref('Clark')
            c_fname.value = 'Lara'
            const greet = `Hello, ${c_fname.value}`
            console.log('c_fname', c_fname)
            return {
                c_fname,
                greet,
            }
        },
        data(){
            return {
                o_fname: 'Nauman'
            }
        },
    }
</script>

<style scoped>

</style>