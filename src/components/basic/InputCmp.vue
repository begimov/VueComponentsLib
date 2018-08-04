<template>
    <input 
        :name="name"
        :id="name"
        :type="type"
        class="form-control"
    >
</template>

<script>
export default {
    props: {
        'name': {
            required: true,
            type: String
        },
        'type': {
            required: false,
            type: String,
            default: 'text'
        }
    }
}
</script>

