<template>
  <div>
    <h1>This is a Home page</h1>
    <Message />
    <Counter :max="10"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Counter from '@/components/Counter.vue'
import Message from '@/components/Message.vue'

export default {
  name: 'HomeView',
  components: {
    Counter,
    Message
}
}
</script>
