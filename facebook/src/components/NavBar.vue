<template>
  <div class="nav-bar-base">
    <img class="logo" src="../assets/logo.png" />
    <search-form />
    <menu-base>
      <img class="user-icon" src="../assets/usagi.jpg" />
      <span class="user-name">denzow</span>
    </menu-base>
    <menu-base>
      <span>ホーム</span>
    </menu-base>
    <menu-base>
      <span>友達を検索</span>
    </menu-base>
    <menu-base :withBorder="false">
      <i class="fas fa-users"></i>
    </menu-base>
    <menu-base :withBorder="false">
      <i class="fas fa-comment"></i>
    </menu-base>
    <menu-base>
      <i class="fas fa-globe-asia"></i>
    </menu-base>
    <menu-base :withBorder="false">
      <i class="fas fa-question-circle"></i>
    </menu-base>
    <menu-base :withBorder="false">
      <i class="fas fa-caret-down"></i>
    </menu-base>
  </div>
</template>

<script>
import SearchForm from './NavBarComponents/SearchForm';
import MenuBase from './NavBarComponents/MenuBase';

export default {
  name: 'NavBar',
  components: {
    SearchForm,
    MenuBase,
  },
};
</script>

<style scoped lang="scss">
.nav-bar-base {
  display: flex;
  flex-direction: row;
  align-items: center;
  background-color: #42b983;
  padding: 0.3rem;
  justify-content: center;
  font-size: 0.9rem;
  color: white;
}

.logo {
  height: 1.2rem;
  margin: 0.2rem;
}

.fas {
  padding-right: 0.3rem;
  font-size: 1.2rem;
  color: #005533;
}

.user-icon {
  height: 1.5rem;
  margin: 0.3rem;
  border-radius: 50%;

}

</style>
