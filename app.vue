<template>
  <div>
    <NuxtRouteAnnouncer />
    <!-- <NuxtWelcome /> -->
     <NuxtLink to="/">首頁</NuxtLink> |
     <NuxtLink to="/about">關於</NuxtLink> |
     <NuxtLink to="/practise">練習</NuxtLink>
    <NuxtPage></NuxtPage>
    <!-- <Card></Card> -->
  </div>
</template>


<script setup>
import '~/assets/all.scss'
</script>
