<script setup>
defineProps({
    title: String,
    price: Number
});
</script>

<template>
  <div class="block">
    <div>Имя {{ title }}</div>
    <div>Информация прайс {{ price }}</div>
  </div>
</template>



