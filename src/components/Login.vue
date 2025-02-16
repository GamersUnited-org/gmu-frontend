<template>
    <div class="login-container">
        <h2>Login</h2>
        <input type="text" v-model="username" placeholder="Username" />
        <input type="password" v-model="password" placeholder="Password" />
        <button @click="login">Login</button>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const username = ref('');
const password = ref('');
const router = useRouter();

const login = () => {
    if (username.value && password.value) {
        router.push('/first');
    } else {
        alert('Please enter credentials');
    }
};
</script>

<style scoped>
.login-container {
    display: flex;
    flex-direction: column;
    width: 200px;
    margin: 50px auto;
}

input,
button {
    margin: 5px 0;
    padding: 8px;
}
</style>