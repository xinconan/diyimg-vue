<template>
  <img :src="src" alt="" :onerror="errorSrc">
</template>

<script>
export default {
  props: ['src', 'errorSrc'],
}
</script>
