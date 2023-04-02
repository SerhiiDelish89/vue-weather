<template>
    <form>
        <label>
        <CustomSelect></CustomSelect>
        </label>
    </form>
</template>

<script>

import CustomSelect from './CustomSelect.vue'

    export default {
        name: 'FormWeather',
        components:{
            CustomSelect,
        }
    }
</script>

<style lang="scss" scoped>

</style>