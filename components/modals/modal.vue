<template lang="pug">
transition(name="modal-fade")
  .modal-overlay(@click="$emit('close-modal')")
    .modal(@click.stop="")
      section.content
        .block-content
          .title
            h3.uppercase profile
            hr
          .subTitle
            h1 I'm a <Strong>UI/UX Designer & Frontend Developer</Strong> from Chiangrai, Thailand. I aim to make a difference through my creative solution.
            hr
          .info
    .close.flex.absolute(@click="$emit('close-modal')")
      ion-icon(class="close-img" name="close-circle-outline")

          //- img.avatar(src="~//static/aont2.png" alt="")
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({})
</script>
<style lang="postcss" scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: end;
  background-color: #3a3737da;
  z-index: 50;
}

.modal {
  background-color: white;
  height: 100%;
  width: 70%;
  margin-top: 0%;
  padding: 60px;
  -webkit-animation: fadein 2s; /* Safari, Chrome and Opera > 12.1 */
  -moz-animation: fadein 2s; /* Firefox < 16 */
  -ms-animation: fadein 2s; /* Internet Explorer */
  -o-animation: fadein 2s; /* Opera < 12.1 */
  animation: fadein 2s;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Firefox < 16 */
@-moz-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Safari, Chrome and Opera > 12.1 */
@-webkit-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Internet Explorer */
@-ms-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Opera < 12.1 */
@-o-keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
.close {
  margin: 0 0 0 0;
}

.close-img {
  font-size: 40px;
  color: black;
  cursor: pointer;
}

.avatar {
  @apply border-8 border-gray-600 rounded-full object-cover;

  width: 150px;
  height: 150px;
}

h3 {
  font-weight: 500;
  font-size: 28px;
  margin: 20px 0;
}
h1 {
  font-weight: 500;
  font-size: 30px;
  margin: 20px 0;
}
h6 {
  font-weight: 500;
  font-size: 28px;
  margin: 20px 0;
}

p {
  font-size: 16px;
  margin: 20px 0;
}

button {
  background-color: #ac003e;
  width: 150px;
  height: 40px;
  color: white;
  font-size: 14px;
  border-radius: 16px;
  margin-top: 50px;
}
.block-content {
  margin: 0 0 70 px;
  overflow: hidden;
}
.content {
  position: relative;
  padding: 120 px 70 px 30 px;
  height: auto;
  overflow: hidden;
}
</style>
