<template>
  <span class="menu-base" :class="{ withBorder: withBorder}">
    <slot></slot>
  </span>
</template>

<script>
export default {
  name: 'MenuBase',
  props: {
    withBorder: {
      type: Boolean,
      default: true,
    },
  },
};
</script>

<style lang="scss" scoped>

.menu-base {
  height: 1.7rem;
  padding-right: 0.5rem;
  padding-left: 0.5rem;
  display: flex;
  align-items: center;
  cursor: pointer;
  &:hover {
    background-color: #22A953;
  }
}

.withBorder {
  border-right: solid 1px #22A953;
}
</style>
