<template>

<p class="rank">Reaction Time is {{score}} <br/>{{rank}}</p>  
</template>

<script>
export default {
    props:['score'],
    data(){
        return{
            rank: null
        }
    },
    mounted(){
        if(this.score < 250){
            this.rank ="Ninja reaction master"
        }
        else if(this.score < 450){
        this.rank ="rapid reflexes"
        }
        else{
            this.rank = "snail pace"
        }

    }
    

}
</script>

<style>
.rank{
    width: 400px;
    border-radius: 20px;
    background: #845ec2;
    text-align: center;
    padding:100px 0;
    margin: 40px auto;
    color:rgb(233,233,233);
}
</style>