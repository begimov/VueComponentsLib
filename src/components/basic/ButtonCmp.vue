<template>
    <router-link 
        class="btn"
        @click.native="clicked"
        :class="[ 
            themes[theme], sizes[size], {'disabled': disabled}
        ]" 
        :to="to">
        <slot>VAL</slot>
    </router-link>
</template>

<script>
export default {
    data() {
        return {
            themes: {
                secondary: 'btn-secondary',
                success: 'btn-success',
            },
            sizes: {
                normal: '',
                large: 'btn-lg',
            },
        }
    },
    props: {
        theme: {
            required: false,
            type: String,
            default: 'secondary'
        },
        size: {
            required: false,
            type: String,
            default: 'normal'
        },
        to: {
            type: Object,
            required: false,
            default() {
                return { name: 'home' }
            }
        },
        disabled: {
            type: Boolean,
            required: false,
            default: false
        },
    },
    methods: {
        clicked (e) {
            this.$emit('click', e)
        }
    }
}
</script>
