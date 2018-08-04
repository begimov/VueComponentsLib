<template>
    <div>
        <input 
            :name="name"
            :id="name"
            :type="inputType"
            class="form-control"
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
    }
}
</script>

