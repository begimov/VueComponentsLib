<template>
    <div>
        <input
            v-bind="$attrs" 
            :name="name"
            :id="name"
            :type="inputType"
            :value="value"
            class="form-control"
            @input="changed"
        >
        <p>
            <a href="#" v-if="type === 'password'" @click.prevent="showPassword = !showPassword">
                {{ showPasswordSwitchText }}
            </a>
        </p>
    </div>
</template>

<script>
export default {
    data () {
        return {
            showPassword: false
        }
    },
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
        'type': {
            required: false,
            type: String,
            default: 'text'
        }
    },
    computed: {
        inputType () {
            return this.showPassword ? 'text' : this.type
        },
        showPasswordSwitchText () {
            return this.showPassword ? 'hide' : 'show'
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

