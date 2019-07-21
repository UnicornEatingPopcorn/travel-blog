<template>
  <div id="app">
    <div class="container">
      <section class="section">
        <h1 class="title title-yellow">
          Welcome to One Click Travel Blog
        </h1>
        <p class="subtitle">
        All photos and videos on our profile in <a href="https://www.instagram.com/one_click_trip">Instagram</a>
        </p>
      </section>
      <div class="pipe"></div>
      <section class="section">
        <div class="timeline">
          <header class="timeline-header">
            <span class="tag is-medium is-warning">Nowadays</span>
          </header>
          <div class="timeline-item is-warning">
            <div class="timeline-marker is-primary"></div>
            <div class="timeline-content">
              <div class="columns">
                <div class="column">
                  <VideoModal/>


                </div>
                <div class="column">
                  <p>Timeline content - Can include any HTML element</p>
                </div>
              </div>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-marker is-image is-32x32">
              <img src="http://bulma.io/images/placeholders/32x32.png">
            </div>
            <div class="timeline-content">
              <p class="heading">February 2016</p>
              <p>Timeline content - Can include any HTML element</p>
            </div>
          </div>
          <header class="timeline-header">
            <span class="tag is-primary">2017</span>
          </header>
          <div class="timeline-item">
            <div class="timeline-marker is-icon">
              <i class="fa fa-flag"></i>
            </div>
            <div class="timeline-content">
              <p class="heading">March 2017</p>
              <p>Timeline content - Can include any HTML element</p>
            </div>
          </div>
          <div class="timeline-header">
            <span class="tag is-medium is-primary">End</span>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import VideoModal from "@/components/VideoModal.vue"

export default {
  components: {
    VideoModal
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
