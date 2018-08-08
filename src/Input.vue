<template>
    <div>
        <input type="text" v-model="message1"> 
        <p>{{message1}}</p>
        <label>Change parent Message: </label><input type="text" :value="msg" @input="changeMessage">
        <p>{{message}}</p>
    </div>
</template>

<script>
    export default {
        props: ['msg'],
        data() {
            return {
                message: '',
                message1: 'io'
            }
        },
        methods: {
            changeMessage(event) {
                this.message = event.target.value
                this.$emit('messageChanged', this.message)
            }
        }
    }
</script>