<script>
    export default {
        props: {
            character: {
                type: Array,
                required: true,
            }
        }
    }
</script>

<template>
    <div>
        <p> {{ character }}</p>
    </div>
</template>