<template>
    <div class="btc">
        <button v-on:click="count++">You clicked me {{ count }} times.</button>
    </div>
</template>
<script>
    export default {
        name: 'ButtonCounter',
        props: {
            count: Number
        }
    }
</script>
