<template>
    <div>
        <input type="text" placeholder="first name" v-model="fname" />
        <input type="text" placeholder="last name" v-model="lname" />


        <input type="text" placeholder="Hero name" v-model="heroName" />
        <input type="text" placeholder="first name" v-model="firstname" />
        <input type="text" placeholder="last name" v-model="lastname" />
    </div>
</template>

<script>
    import { ref, reactive, toRefs} from 'vue'
    export default {
        name: 'VModelComponent',
        setup(){
            const heroName = ref('')
            const state = reactive({
                firstname: '',
                lastname: '',
            })
            return{
                heroName,
                ...toRefs(state)
            }
        },
        data(){
            return{
            fname: '',
            lname: ''
            } 
        }
  }
</script>

<style scoped>

</style>