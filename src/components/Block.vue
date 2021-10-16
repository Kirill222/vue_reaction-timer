<template>
  <div class="block" v-if="showBlock">
      click me
  </div>
</template>

<script>
export default {
    props: ['delay'],
    data() {
        return {
            showBlock: false,
        }
    },
    //lifecycle hooks are written here too
    mounted() {
        console.log("mounted")
        setTimeout(()=> {
            this.showBlock = true
        }, this.delay)
    },
    updated() {
        console.log("updated")
    },
    unmounted() {
        console.log("unmounted")
    }
} 
</script>

<style>

    .block {
        width: 400px;
        border-radius: 20px;
        background: #0faf87;
        color: white;
        text-align: center;
        padding: 100px 0;
        margin: 40px auto;
    }

</style>