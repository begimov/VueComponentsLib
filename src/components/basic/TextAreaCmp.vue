<template>
    <textarea
        v-bind="$attrs" 
        :name="name"
        :id="name"
        :value="value"
        :rows="rows"
        class="form-control"
        @input="changed"
    ></textarea>
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
        },
        'minHeight': {
            required: false,
            type: String,
            default: "3"
        }
    },
    methods: {
        changed (e) {
            this.$emit('input', e.target.value)
        }
    },
    computed: {
        rows () {
            return Math.max(this.minHeight, this.value.split("\n").length)
        }
    },
    mounted () {
        //
    }
}
</script>

