<script setup>

defineProps({
    imageUrl: String,
    title: String,
    price: Number,
    isLike: Boolean,
    isCart: Boolean,
    setIsLike: Function,
    setIsCart: Function
});

</script>

<template>
    <div class="flex flex-col items-stretch box-border cursor-pointer pt-5 px-8 pb-8 relative bg-white max-w-52 rounded-3xl border border-slate-200 hover:-translate-y-2 hover:shadow-lg duration-300">
        <div class="absolute top-7 left-7 hover:scale-110 duration-200">
            <img :src="isLike ? '/like-2.svg' : '/like-1.svg'" v-on:click="setIsLike" alt="добавить в избранное">
        </div>
        <div class="w-32 h-28 mb-3.5">
            <img class="max-w-full" :src="imageUrl" alt="">
        </div>
        <div class="text-sm text-black mb-3.5">{{title}}</div>
        <div class="flex justify-between">
        <div class="flex flex-col">
            <div class="text-xs text-slate-400">Цена:</div>
            <div class="text-sm font-bold">{{price}} руб.</div>
        </div>
        <div class="hover:scale-110 duration-200">
            <img :src="isCart ? '/checked.svg' : '/plus.svg'" v-on:click="setIsCart" alt="добавить в корзину">
        </div>
        </div>
    </div>
  </template>