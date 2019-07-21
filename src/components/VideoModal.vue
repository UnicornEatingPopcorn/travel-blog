<template lang="pug">
  div
    .container(id="launch-modal")
      .content.has-text-centered
        p.control
          button(v-on:click="launch" class="button is-primary") Launch modal
    .modal(v-bind:class="{'is-active':isActive}" @click="close")
      .modal-background
        .modal-content
          .box
            .content.has-text-centered
              p.control
                h3 {{message}}
</template>

<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    launch: function() {
      this.isActive = true;
    },
    close: function(event) {
      if((event.target).closest(".container")) {
      this.isActive = false
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
