<template>
    <router-link 
        class="btn"
        :class="{ 'btn-secondary': secondary, 'btn-success': success }" 
        :to="to">
        PAGE
    </router-link>
</template>

<script>
export default {
    props: {
        secondary: {
            required: false,
            type: Boolean,
            default: true
        },
        success: {
            required: false,
            type: Boolean,
            default: false
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
