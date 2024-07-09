
<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
    </h3>
  </div>
  <div ></div>
</template>

<script>
export default {
  props: {
    msg: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      localMsg: 'Hello',
      id:'aaa00'
    }
  }
}
</script>