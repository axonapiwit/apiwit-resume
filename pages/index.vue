<template lang="pug">
section.bg-hero(class="h-screen bg-center bg-cover" style="background-image: url('/siraont.jpg')")
  .overlay
  .container
    .name-block
      .name-block-container.space-y-3
        .text-white.text-2xl Hi, i'm
        span.title.font-bold apiwit thammachai
        h4.sub-title.font-bold DESIGNER & DEVELOPER
        .button.bg-gray-500.flex.justify-center.items-center.space-x-2.p-3.w-56.cursor-pointer
          .text-white.uppercase download resume
          img.mt-1.w-6(src="~//static/icons/download.png" alt="")
        .link.flex.justify-between.items-center.w-52
          a(href="https://www.facebook.com/axon.apiwit")
            img.fb-icon(src="~//static/icons/facebook-icon.png" alt="")
          a(href="https://www.instagram.com/sir.aont")
            img.ig-icon(src="~//static/icons/instagram-icon.png" alt="")
          a(href="https://github.com/axonapiwit")
            img.gh-icon(src="~//static/icons/github-icon.png" alt="")
    .menu-blocks
      .about-block.menu-block(@click="showModal = true")
        .about-block-container
          h1.about.menu-item resume
      .portfolio-block.menu-block
        .portfolio-block-container
          h1.portfolio.menu-item portfolio
      .contact-block.menu-block
        .contact-block-container
          h1.contact.menu-item contact

  Modal(v-show="showModal" @close-modal="showModal = false")

</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import Modal from '@/components/modals/modal.vue'
export default defineComponent({
  components: { Modal },
  data() {
    return {
      showModal: false,
    }
  },
})
</script>

<style lang="postcss" scoped>
.bg-hero {
  width: 100%;
  height: 100vh;
  position: fixed;
  overflow: hidden;
  background-size: cover;
  z-index: 0;
}
.overlay {
  background-color: rgba(0, 0, 0, 1);
  height: 100%;
  position: fixed;
  width: 100%;
  opacity: 0.35;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-right: 15px;
  padding-left: 15px;
  width: 100%;
}
@media (min-width: 1025px) and (max-width: 1920px) {
  .name-block {
    -ms-transform: rotate(-34deg);
    -webkit-transform: rotate(-34deg);
    transform: rotate(-34deg);
    left: -200px;
    top: -80px;
  }
}
.name-block {
  position: absolute;
  width: 693px;
  height: 700px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-right: none;
  display: table;
  transition: all 0.5s;
  z-index: 1;
}
.name-block-container {
  display: table-cell;
  vertical-align: middle;
  padding-left: 240px;
  -ms-transform: rotate(34deg);
  -webkit-transform: rotate(34deg);
  transform: rotate(34deg);
}
.menu-blocks {
  transition: all 0.5s;
}
@media (min-width: 1025px) and (max-width: 1920px) {
  .about-block {
    -ms-transform: rotate(-34deg);
    -webkit-transform: rotate(-34deg);
    transform: rotate(-34deg);
    left: 419px;
    top: -160px;
    width: 350px;
    height: 300px;
  }
}
.about-block {
  position: absolute;
  width: 430px;
  height: 300px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-bottom: none;
  transition: all 0.5s;
  z-index: 1;
}
.menu-block {
  @apply uppercase;

  cursor: pointer;
}
.menu-block:hover {
  border: 15px solid rgba(3, 148, 126, 0.219);
}

.about-block-container {
  vertical-align: middle;
  padding: 150px 0 0 70px;
  -ms-transform: rotate(34deg);
  -webkit-transform: rotate(34deg);
  transform: rotate(34deg);
}
h1.menu-item {
  position: relative;
  color: #fff;
  margin: 50px;
  font-size: 28px;
  font-weight: 600;
  transition: all 1s ease-out;
}
@media (min-width: 1025px) and (max-width: 1920px) {
  .portfolio-block {
    -ms-transform: rotate(-34deg);
    -webkit-transform: rotate(-34deg);
    transform: rotate(-34deg);
    left: 586px;
    top: 88px;
    width: 350px;
    height: 300px;
  }
}
.portfolio-block {
  position: absolute;
  width: 430px;
  height: 300px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  display: table;
  transition: all 0.5s;
  z-index: 1;
}
.portfolio-block-container {
  display: table-cell;
  vertical-align: middle;
  -ms-transform: rotate(34deg);
  -webkit-transform: rotate(34deg);
  transform: rotate(34deg);
}
@media (min-width: 1025px) and (max-width: 1920px) {
  .contact-block {
    -ms-transform: rotate(-34deg);
    -webkit-transform: rotate(-34deg);
    transform: rotate(-34deg);
    left: 753px;
    top: 335px;
    width: 350px;
    height: 300px;
  }
}
.contact-block {
  position: absolute;
  width: 430px;
  height: 300px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  display: table;
  transition: all 0.5s;
  z-index: 1;
}
.contact-block-container {
  display: table-cell;
  vertical-align: middle;
  padding-left: 50px;
  -ms-transform: rotate(34deg);
  -webkit-transform: rotate(34deg);
  transform: rotate(34deg);
}

.title {
  @apply uppercase;

  display: block;
  font-size: 40px;
  letter-spacing: 1px;
  color: white;
}
.sub-title {
  @apply uppercase;

  display: block;
  font-size: 24px;
  letter-spacing: 1px;
  color: white;
}
.fb-icon {
  width: 45px;
  cursor: pointer;
}
.ig-icon {
  width: 50px;
  cursor: pointer;
}
.gh-icon {
  width: 30px;
  cursor: pointer;
}
</style>
