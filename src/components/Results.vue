<template>
    <p>Your reaction time {{reactionTime}}</p>
    <br>
    <span>{{rank}}</span>
</template>

<script>
export default {
    props: ['reactionTime'],
    data() {
        return {
            rank: null,
        }
    },
    mounted() {
        if (this.reactionTime < 250) {
            this.rank = "Awesome"
        } else if (this.reactionTime < 400) {
            this.rank = "Not bad"
        } else if (this.reactionTime < 600) {
            this.rank = "Try better"
        } else {
            this.rank = "You are slow"
        }
    }
}
</script>

<style>

</style>