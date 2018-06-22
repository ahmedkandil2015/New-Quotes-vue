<template>
    <div class="row">
        <app-qoute v-for="(quote,index) in quotes" :key="quote" @click.native="deleteQuote(index)"> {{ quote }}</app-qoute>
    </div>
</template>
<script>
import Quote from "./Quote.vue";
export default {
  props: ["quotes"],
  components: {
    appQoute: Quote
  },
  methods: {
    deleteQuote(index) {
      this.$emit("quoteDeleted", index);
    }
  }
}
</script>
<style>
</style>
