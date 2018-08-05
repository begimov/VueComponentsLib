<template>
    <div>
        <input
            v-bind="$attrs" 
            :name="name"
            :id="name"
            :value="value"
            class="form-control"
            @input="changed"
        >
    </div>
</template>

<script>
export default {
    props: {
        'value': {
            required: false,
            type: String,
            default: ''
        },
        'name': {
            required: true,
            type: String
        }
    },
    methods: {
        changed (e) {
            this.$emit('input', e.target.value)
        }
    },
    mounted () {
        //
    }
}
</script>

