<script setup>
import {ref} from 'vue'
import { useRouter } from 'vue-router';
const router = useRouter()
const player = ref('');
const login = () => {
    localStorage.setItem("isLoggedIn", 1);
    alert("logged in" + player.value)
    router.push({
        name: 'game'
    })

}

</script>

<template>

     <form class="login" action="" @submit.prevent="login">
         <h1>Login</h1>
         <input type="text" placeholder="enter your name" v-model="player" >
         <div>
             {{player}}
         </div>
         <button>Play</button>
     </form>

</template>

<style scoped>
    .login{
    }
    input {
        padding: 10px;
        margin: 35px;
    }

    button {
        padding: 10px 30px;
        background-color: steelblue;
        color: white
    }
</style>
