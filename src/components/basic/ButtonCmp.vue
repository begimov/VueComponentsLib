<template>
    <router-link class="btn btn-secondary" :to="to">PAGE</router-link>
</template>

<script>
export default {
    props: {
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
