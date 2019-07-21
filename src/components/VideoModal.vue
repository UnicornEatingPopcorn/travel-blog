<template lang="pug">
  div
    .container(id="launch-modal")
      .content.has-text-centered
        p.control
          button(v-on:click="launch" class="button is-primary") Launch modal
    .modal(v-bind:class="{'is-active':isActive}")
      .modal-background
        .modal-content
          .box
            .content.has-text-centered
              p.control
                h3 {{message}}
        button(@click="close" class="modal-close")
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
    close: function() {
      this.isActive = false;
    }
  },
  computed: {
    // Vue.document.click(function(event)) {
    //   if (!(event.target).closest(".modal").length)) {
    //     this.isActive = false
    //   }
    // },

    message: function() {
      return "Hello Bulma Modal";
    }
  }
}
</script>

<style lang="sass">
</style>
