<template>
  <div class="bg-huawei-card p-6 rounded-lg shadow-lg text-white">
    <h2 class="text-xl font-bold mb-2">{{ message.phone }}</h2>
    <p class="truncate text-md">{{ message.content }}</p>
  </div>
</template>

<script>
export default {
  name: "messageCard",
  props: {
    message: Object,
  }
}
</script>

<style scoped>

</style>