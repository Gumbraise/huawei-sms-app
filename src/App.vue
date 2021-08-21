<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <message-list/>
</template>

<script>
import messageList from "./components/messages-card/messageList";

export default {
  name: 'App',
  components: {
    messageList
  }
}
</script>