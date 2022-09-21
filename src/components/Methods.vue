<template>
    <div>
        <h2>{{name}}</h2>
        <button @click="setname">Change Name</button>
        <h2>{{count}}</h2>
        <button @click="increCount">Increment Count</button>

        <h2>{{first}} {{last}}</h2>
        <button @click="changeHero">Change Hero</button>
    </div>
</template>

<script>
    import { ref, reactive, toRefs} from 'vue'
    export default {
        name: 'MethodsComponent',
        setup(){
            const count = ref(0)
            const state = reactive({
                first: 'Ragnar',
                last: 'Bruce'
            })
            function increCount() {
                count.value++
            }

            function changeHero() {
                state.first = 'R',
                state.last = 'L'
            }
            return{
                count,
                increCount,
                ...toRefs(state),
                changeHero
            }
        },
        data(){
            return{
                name: 'Nauman',
            }
        },
        methods: {
            setName(){
                this.name = 'Ragnar'
            },
        },
    }
</script>

<style scoped>

</style>