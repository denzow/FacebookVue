<template>
  <div class="search-form">
    <input type="text" value="" class="search-box"
           @focus="isFocused = true"
           @blur="isFocused = false"/>
    <div class="search-icon" :class="{ focused: isFocused }">
      <i class="fas fa-search" :class="{ focusedIcon: isFocused }"></i>
    </div>
  </div>
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
  border-radius: 0.1rem;
  padding-left: 0.5rem;
  height: 1.5rem;
  display: flex;
  align-items: center;
}

.search-box {
  border: 0;
  width: 85%;
  outline: 0;
  padding: 0;
  height: 100%;
}

.search-icon {
  color: #42b983;
  height: 100%;
  font-size: 1rem;
  width: 15%;
  padding: 0 0.2rem 0 0.5rem;
}

.focused {
  background-color: #88CC99;
}

.focusedIcon {
  color: white;
}
</style>
