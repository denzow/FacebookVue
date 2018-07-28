<template>
  <div class="autocomplete-area">
    <div class="name-area-header">
      <span class="search-label">最近の検索</span>
      <a href="#" class="edit-label">編集する</a>
    </div>
    <div class="name-area" v-for="name in searchHistoryList" :key="name">
      <i class="fas fa-search"></i>
      {{ name }}
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'AutoCompleteArea',
  computed: {
    ...mapState(['searchHistoryList']),
  },
}
</script>

<style lang="scss" scoped>
a {
  text-decoration: none;
}

.fa-search {
  color: grey;
  margin-left: 0.2rem;
}
.name-area-header {
  color: #333333;
  background-color: #EEEEEE;
  font-weight: bold;
  display: flex;
  padding: 0.2rem 0.5rem 0.2rem 0.5rem;
  .edit-label {
    margin-left: auto;
    color: #333333;
    &:hover {
      text-decoration: underline;
    }
  }
}


.name-area {
  color: black;
  padding: 0.4rem;
  cursor: pointer;
  &:hover {
    background-color: #EEEEEE;
  }
}

.autocomplete-area {
  width: 15.5rem;
  position: absolute;
  top: 1.5rem;
  left: -0.1rem;
  box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.4);
  background-color: white;
  font-size: 0.8rem;
}
</style>