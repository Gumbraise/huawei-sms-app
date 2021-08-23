<template>
  <div class="bg-huawei-card p-6 rounded-lg shadow-lg text-white relative">
    <div class="mb-2 flex">
      <h2 class="text-xl font-bold w-1/2">{{ message.phone }}</h2>
      <p
          class="text-md w-1/2 text-right text-gray-400"
      >{{ message.date }}</p>
    </div>

    <p
        :class="message.smstat ? 'truncate' : 'font-bold'"
        class="text-md"
    >{{ message.content }}</p>
  </div>
</template>

<script>
export default {
  name: "messageCard",
  props: {
    message: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>

</style>