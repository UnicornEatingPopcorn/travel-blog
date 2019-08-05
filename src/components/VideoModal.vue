<template lang="pug">
  .modal(v-on:click="close")
     .modal-background
     .modal-content
       .box
         .content.has-text-centered
           p.control
             h3 {{message}}
</template>

<script>
export default {
  methods: {
    close: function(event) {
      debugger
      if((event.target).closest(".modal")) {
        (event.target).closest(".modal").classList.toggle("is-active")
      }
    }
  },
  computed: {
    message: function() {
      return "Hello Bulma Modal";
    }
  }
}
</script>

<style lang="sass">


</style>
