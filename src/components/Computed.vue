<template>
    <div>
        <input type="text" placeholder="F Name" v-model="fName" />
        <input type="text" placeholder="L Name" v-model="lName" />
        <h2>Options Full Name is {{fullName}}</h2>
    </div>
</template>

<script>
    export default {
        name: 'ComputedComponent',
        data(){
            return {
                fName: '',
                lName: '',
            }
        },
        computed:{
            fullName(){
                return `${this.fName} ${this.lName}`
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>