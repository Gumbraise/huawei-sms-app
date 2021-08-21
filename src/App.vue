<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <messages/>
</template>

<script>
import messages from "./components/messages";

export default {
  name: 'App',
  components: {
    messages,
  },
}
</script>