<template>
    <div class="container">
<slot>Default value</slot>
    </div>
</template>

<script>
    export default {
        name: 'ContainerWeather',
    }
</script>

<style lang="css" scoped>
 .container{
     max-width: 450px;
    margin: 0 auto;
    background-color: cornflowerblue;
 }
</style>