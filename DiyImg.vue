<template>
  <img :src="src" ref="DiyImg" :alt="alt" @error="onImgErr">
</template>

<script>
export default {
  name: 'DiyImg',
  props: {
    alt: String,
    src: String,
    errorSrc: String
  },
  methods: {
    onImgErr () {
      this.$refs.DiyImg = this.errorSrc
    }
  }
}
</script>
