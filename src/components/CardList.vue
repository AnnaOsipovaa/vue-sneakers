<script setup>

import Card from './Card.vue';

function setIsLike(){
    alert('setIsLike');
}
function setIsCart(){
    alert('setIsCart');
}
</script>

<template>
      <div class="grid grid-cols-4 gap-5">
        <Card 
            :is-like="true" 
            :is-cart="true" 
            imageUrl="../../public/sneakers/sneakers-1.jpg" 
            title="12345" 
            :price="1223" 
            :set-is-like="setIsLike"
            :set-is-cart="setIsCart" />
      </div>
</template>  