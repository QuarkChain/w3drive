<template>
  <svg
    v-bind="$attrs"
    v-on="$listeners"
    class="go-icon"
    aria-hidden="true"
    :color="this.color"
  >
    <use :xlink:href="`#${name}`"></use>
  </svg>
</template>

<script>
import '../utils/svg';

export default {
  name: 'UploadIcon',
  inheritAttrs: false,
  props: {
    name: {
      type: String,
      required: true
    },
    color: {
      type: String,
    }
  },
};
</script>

<style lang="scss" scoped>
.go-icon {
  width: 1em; height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
</style>
