<template>
    <form>
      <div class="icon-container">
        <img class="icon-image" src="../images/user.png" />
        <h2>Admin</h2>
      </div>
    <div class="input-class">  
       <input type="text"  placeholder="Enter Email..."  v-model="email" />
    </div>
     <div class="input-class">
        <i class="small-icon2"></i> 
        <input type="password" placeholder="Enter Password..." v-model="password" />
    </div>
    <button>LOG IN</button>
<footer>Copyright&copy;2023</footer>
</form>

</template>

<script>
import {ref} from 'vue'
    export default {
        name:'ButtonComp',
        
        setup(){
            const email=ref('')
            const password=ref('')

            return{ 
            email,
            password
        }
           
        }
    }
</script>

<style scoped>
form{
    text-align:center;
    height:100vh;
    line-height:1em;
}
.icon-container{
    width:50px;
    height:50px;
    position:relative;
    top:23%;
    left:47%;
}
.icon-image{
    width:80px;
}
.input-class{
    left:-100%;
    text-align:center;
    position:relative;
    top:30%;
    animation: input 0.5s linear 1s forwards;
}
input[type=text]{
    padding:10px;
    width:400px;
}
input[type=password]{
    margin-top:30px;
    padding:10px;
    width:400px;
}
button{
    text-align:center;
    position:relative;
    top:35%;
    left:44%;
    display:block;
    width:180px;
    font-size:1rem;
    padding:15px;
    /* text-transform:uppercase; */
    color:white;
    cursor:pointer;
    opacity:0;
    /* border:none; */
    background:transparent;
    background-image:linear-gradient(to right,white 50%,transparent 50%);
    background-position:100% 0%;
    background-size:200% 100%;
    transition:0.6s;

    animation:fadeIn 1s linear 2s forwards;
}
button:hover{
    color:black;
    text-transform:uppercase;
  background-position:0% 50%;
}

@keyframes fadeIn{
    from{opacity:0;}
    to{opacity:1;}
}

@keyframes input{
    from{left:-100%}
    to{left:-0%}
}
@keyframes fallIn{
    from{top:-100%}
    to{top:0%}
}

footer{
    position:relative;
    top:60%;
    color:white;
    font-style:bold;
    font-size:1.3rem;
}
</style>