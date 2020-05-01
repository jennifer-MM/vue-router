<template>
  <div class="reverse">
    <h1>This is the reverse page</h1>
    <h2>Please enter a string to reverse!</h2>
    <label>
      String:
      <input type="text" id="string" v-model.lazy="message" /> 
    </label>

    <h2>That string, reverse, is:</h2>
    <p>{{ reversedMessage }}</p>
  </div>
</template>

<script>
export default {
  name: "Reverse",
  data() {
    return {
      message: ""
    };
  },
  computed: {
    reversedMessage() {
      return this.message
        .split("")
        .reverse()
        .join("");
    }
  }
};
</script>