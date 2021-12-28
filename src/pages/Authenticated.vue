<script setup>
        import { useRouter } from 'vue-router';
    const isLoggedIn = !!localStorage.getItem("isLoggedIn")
    if (!isLoggedIn) {
        useRouter().push({name: "login"})
    }
</script>

<template>
<div>

  <router-view />
</div>
</template>

<style>

</style>
