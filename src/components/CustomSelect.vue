<template>
 <select v-model="selected">
    <option value="Sydney">Sydney</option>
                <option value="Melbourne">Melbourne</option>
                <option value="Brisbane">Brisbane</option>
                <option value="Perth">Greater Perth</option>
                <option value="Adelaide">Greater Adelaide</option>
                <option value="Canberra">Canberra</option>
                <option value="Hobart">Hobart</option>
                <option value="Darwin">Darwin</option>
 </select>
</template>

<script>
    export default {
       name: 'CustomSelect', 
       props:{
        items:{
            type: Array,
            required: true,
        }
       },
    //    computed:{
    //     listeners(){
    //         return{
    //             ...this.listeners,
    //                  input: event =>this.$emit('input', event.target.value)
    //         }
    //     },
    //     formatedItems(){
    //         return this.items.map(item =>{
    //             return t
    //         })
    //     }
    //    }
    }
</script>

<style lang="scss" scoped>

</style>