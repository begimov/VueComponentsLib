<template>
    <div class="modal-cmp">
        <div class="modal-cmp-body p-4 text-center">
            //
        </div>
    </div>
</template>

<script>
export default {
    props: {
        //
    },
    methods: {
        //
    },
    computed: {
        //
    },
    mounted () {
        //
    }
}
</script>

<style>
    .modal-cmp {
        background-color: #00000099;
        position: fixed;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        z-index: 9999;
    }
    .modal-cmp-body {
        position: fixed;
        top: 50%;
        left: 50%;
        background-color: white;
        width: 90%;
        max-width: 600px;
        transform: translate(-50%, -50%);
    }
</style>


