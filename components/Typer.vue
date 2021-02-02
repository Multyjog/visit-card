<template>
  <textarea
    @keydown.prevent="increaseCounter()"
    @keydown.backspace.prevent="decreaseCounter()"
    :value="visibleText"
    rows="3"
  ></textarea>
</template>

<script>
export default {
  data() {
    return { counter: 0 };
  },
  methods: {
    increaseCounter() {
      this.counter = Math.min(this.counter + 9, this.text.length);
    },
    decreaseCounter() {
      this.counter = Math.max(this.counter - 18, 0);
    }
  },
  computed: {
    visibleText() {
      return this.text.substring(0, this.counter);
    }
  },
  props: ["text"]
};
</script>

<style scoped>
textarea {
  width: 100%;
  height: 260px;
}
</style>
