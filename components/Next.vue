<template>
<v-icon @click="showNext" id="right-mid" >mdi-chevron-right</v-icon>
</template>

<script>
export default {
data(){
    return{}
},
methods:{
    showNext(){
        this.$emit("clicked",true)
        
    }
}
}
</script>

<style>
#right-mid{
    position: fixed;
    top: 40vh;
    right: 7vw;
    color: #a64de9;
    font-size: 6rem;
}
</style>