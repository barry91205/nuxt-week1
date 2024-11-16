<script setup>
const { data, status, error, refresh, clear } = await useFetch('https://randomuser.me/api/')
console.log(data);

const isLoading = ref(true);
setTimeout(() => {
    isLoading.value = false;
},2000);
// Import component
// import Loading from 'vue-loading-overlay
// Import stylesheet
// import 'vue-loading-overlay/dist/vue-loading.css';
</script>
<template>
    <div>
        <h1>Nuxt 3</h1>
        
        {{ data }}
        <button type="buuton" @click="refresh">重新整理</button>

        <h2>以下是伺服器渲染</h2>
        <ClientOnly>
            <!-- Loading在這裡面才不會跳出錯誤 -->
            <Loading :active="isLoading"></Loading>
            <h1>伺服器渲染的文字</h1>
        </ClientOnly>
    </div>
</template>   