<template>
    <div>
        <h1>Welcome to First Page</h1>
        <button @click="logout">Logout</button>
    </div>
</template>

<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();
const logout = () => {
    router.push('/');
};
</script>