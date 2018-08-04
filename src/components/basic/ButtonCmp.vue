<template>
    <router-link 
        class="btn"
        :class="[ 
            themes[theme], sizes[size]
        ]" 
        :to="to">
        PAGE
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
        }
    }
}
</script>
