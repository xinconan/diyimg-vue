<template>
  <img :src="imgSrc" @error="onImgErr" :mode="mode">
</template>

<script>
export default {
  name: 'DiyImg',
  props: {
    src: String,
    errorSrc: String,
    mode: {
      type: String,
      default: 'aspectFit'
    }
  },
  data () {
    return {
      imgSrc: this.src
    }
  },
  methods: {
    onImgErr () {
      // not supported in miniapp
      // this.$refs.DiyImg.src = this.errorSrc
      this.imgSrc = this.errorSrc
    }
  }
}
</script>
