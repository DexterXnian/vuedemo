
<template>
  <div class="greetings" v-if="flag">
    <h1 class="green">{{ msg }}</h1>
    <h3>You’ve successfully created a project with</h3>
  </div>
  <div class="greetings" v-else>
    <h1 class="green">{{ msg }}</h1>
    <h3>那你还是看看我吧</h3>
  </div>
  <div class="greetings" v-show="flag">
    <h1 class="green">{{ msg }}</h1>
    <h3>那你还是看看我吧</h3>
  </div>
</template>

<script>
export default {
    props: {
        msg: {
        type: String,
        required: true,
        },
    },
    data() {
        return {
        flag: false,
        id: "aaa00",
        };
    },
    };
</script>