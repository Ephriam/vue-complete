<template>
    <div>
        <h1>This is a greate message!</h1>
        <app-input :msg="message" @messageChanged="message=$event"></app-input>
        <p>{{message}}</p>   
    </div>
</template>
<script>
    import Input from './Input.vue'
    export default {
        data() {
            return {
                message: 'live message'
            }
        },
        components: {
            'app-input': Input
        }
    }
</script>