<template>
  <div @mouseover="showTooltip = true" @mouseout="showTooltip = false">
    <slot name="displayContent" />
    <slot />
    <span class="tooltipContent" v-show="showTooltip">
      <slot name="tooltipContent" v-if="!content"/>
      <span v-if="content">{{ content }}</span>
    </span>
  </div>
</template>

<script>
export default {
  name: 'Tooltip',
  props: {
    content: {
      type: String,
      default: null,
    }
  },
  data() {
    return {
      showTooltip: false,
    };
  }
}
</script>

<style lang="scss" scoped>
  .tooltipContent {
    word-break: keep-all;
    display: block;
    position: absolute;
    top: 30px;
    font-size: 90%;
    color: #fff;
    background-color: #112211;
    padding: 0.3rem 1rem 0.3rem 1rem;
    border-radius:3px;
    z-index:100;
    &:before {
      content:'';
      display:block;
      position:absolute;
      height:0;
      width:0;
      top:-13px;
      left:7px;
      border:13px transparent solid;
      border-right-width:0;
      border-left-color:#112211;
      transform:rotate(270deg);
      z-index:100;
    }
  }
</style>