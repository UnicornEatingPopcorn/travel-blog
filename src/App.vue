<template lang="pug">
#app
  .container
    section.section
      h1.title.title-yellow
        | Welcome to One Click Travel Blog
      p.subtitle
        | All photos and videos on our profile in
        a(href='https://www.instagram.com/one_click_trip')  Instagram
    .pipe
    section.section
      .container
        .timeline
          header.timeline-header
            span.tag.is-medium.is-warning Nowadays
          .timeline-item.is-warning
            .timeline-marker.is-primary
            .timeline-content
              .tile.is-ancestor
                .tile.is-vertical.is-8
                  .tile
                    .tile.is-parent.is-vertical
                      article.tile.is-child.notification.is-primary
                        p.title Vertical...
                        p.subtitle Top tile
                      article.tile.is-child.notification.is-warning
                        p.title ...tiles
                        p.subtitle Bottom tile
                    .tile.is-parent
                      article.tile.is-child.notification.is-info
                        figure.image.is-6
                          img(src="https://bulma.io/images/placeholders/640x480.png")
                  .tile.is-parent
                    article.tile.is-child.notification.is-danger
                      p.title Wide tile
                      p.subtitle Aligned with the right tile
                      .content
                        // Content
                .tile.is-parent
                  article.tile.is-child.notification.is-success
                    figure.image.is-16by9
                      iframe.has-ratio(width="640" height="360" src="https://www.youtube.com/embed/YE7VzlLtp-4?showinfo=0" frameborder="0" allowfullscreen)
            //- .columns
            //-   .column
            //-     a(id="launch-modal" v-on:click="launch")
            //-       figure.image.is-5by4
            //-         img(src="https://i.imgur.com/CpUmo0Q.jpg")
            //-     VideoModal(v-bind:class="{'is-active':isActive}")
            //-
            //-   .column
            //-     p Timeline content - Can include any HTML element
        .timeline-item
          .timeline-marker.is-image.is-32x32
            img(src='http://bulma.io/images/placeholders/32x32.png')
          .timeline-content
            p.heading February 2016
            p Timeline content - Can include any HTML element
        header.timeline-header
          span.tag.is-primary 2017
        .timeline-item
          .timeline-marker.is-icon
            i.fa.fa-flag
          .timeline-content
            p.heading March 2017
            p Timeline content - Can include any HTML element
        .timeline-header
          span.tag.is-medium.is-primary End
</template>

<script>
import VideoModal from "@/components/VideoModal.vue"

export default {
  components: {
    VideoModal
  },
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    launch: function() {
      this.isActive = true;
    }
  },
  name: 'app'
 }
</script>

<style lang="sass">
body
  background-color: #201502

.pipe
  height: 1px
  background: #ffdd57
  width: 100%

.title-yellow
  color: #ffdd57 !important
</style>
