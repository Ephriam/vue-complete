<template>
    <div>
        <h1>Users Page!!</h1>
        <p>Team Id: {{$route.params.teamId}}</p>
    </div>
</template>

<script>
    export default {
        created() {
            this.goHome()
            console.log(this.$route.params.teamId)
        },
        watch: {
            '$route'(to, from) {
                console.log(to.params.teamId)
            }
        },
        methods: {
            goHome() {
                setInterval(()=>{
                   this.$router.push('/') 
                }, 5000)
                
            }
        }
    }
</script>