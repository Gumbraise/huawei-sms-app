<template>
  <div class="space-y-4">
    <message-card

        v-for:="(message, i) in xml"
        :v-key="i"
        :message="message"
    />
  </div>
</template>

<script>
import messageCard from "./messageCard";

export default {
  name: "messageList",
  components: {
    messageCard,
  },
  props: {
    xml: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>

</style>