<template>
  <span class="search-form">
    <input type="text" value="" class="search-box"
           @focus="isFocused = true"
           @blur="isFocused = false"/>
    <i class="fas fa-search" :class="{ focusedIcon: isFocused }"></i>
  </span>
</template>

<script>
export default {
  name: 'SearchForm',
  data() {
    return {
      isFocused: false,
    };
  }
};
</script>

<style lang="scss" scoped>
.search-form {
  width: 12rem;
  margin-right: 5rem;
  background-color: white;
  border-radius: 0.3rem;
  padding-left: 0.5rem;
  height: 1.5rem;
}

.search-box {
  border: 0;
  width: 85%;
  outline: 0;
  padding: 0;
  height: 100%;
}

.fas {
  color: #42b983;
  height: 100%;
  font-size: 1rem;
  width: 15%;
}

.focusedIcon {
  background-color: #42b983;
  color: white;
}
</style>
