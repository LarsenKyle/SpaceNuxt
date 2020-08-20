<template>
<v-icon @click="showNext" id="back-mid" >mdi-chevron-left</v-icon>
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
#back-mid{
    position: fixed;
    top: 40vh;
    right: 7vw;
    color: white;
    font-size: 6rem;
}
</style>