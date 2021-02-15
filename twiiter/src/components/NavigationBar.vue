<template>
    <div class="menu">
     <nav>
        <a href="#">Ninja Reaction Timer</a>
    
     </nav>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
*{
    margin:0;
    padding:0;
    box-sizing: border-box;
}
body{
 
    background: linear-gradient(to right,#3c1053,#ad5389);
        height:100vh;
        display: inline-block;

}
.menu{
    position: absolute;
    top:40px;
    left: 50%;
    transform: translate(-50%,-50%);

}
.menu a{
    color: rgb(233,233,233);
    text-decoration: none;
    font-size: 1.5rem;
    margin:20px;
    padding: 15px 30px;
    background: rgba(255,255,255,0.055);
    position: relative;
    transition: all .5s;
}
.menu a:hover{
    box-shadow: 0 20px 30px rgba(0, 0, 0, 0.24);
}

.menu a::before{
    content:'';
    position: absolute;
    bottom:0;
    left: 0;
    width: 100%;
    height:0%;
    background: #845ec2;
 
    transition: all .4s;

}
.menu a:hover::before{
    height: 50%;
}
</style>