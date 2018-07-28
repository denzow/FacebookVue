<template>
  <div class="nav-bar-base">
    <div class="logo">
      <i class="fab fa-facebook-f"></i>
    </div>
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
      <tooltip content="友達リクエスト">
        <i class="menu-icon fas fa-users" slot="displayContent"></i>
      </tooltip>
    </menu-base>
    <menu-base :withBorder="false">
      <tooltip content="メッセージ">
        <i class="menu-icon fas fa-comment"></i>
      </tooltip>
    </menu-base>
    <menu-base>
      <tooltip content="お知らせ">
        <i class="menu-icon fas fa-globe-asia"></i>
      </tooltip>
    </menu-base>
    <menu-base :withBorder="false">
      <tooltip content="クイックヘルプ">
        <i class="menu-icon fas fa-question-circle"></i>
      </tooltip>
    </menu-base>
    <menu-base :withBorder="false">
      <i class="menu-icon fas fa-caret-down"></i>
    </menu-base>
  </div>
</template>

<script>
import SearchForm from './NavBar/SearchForm';
import MenuBase from './NavBar/MenuBase';

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
  height: 1.5rem;
  width: 1.5rem;
  color: #42b983;
  background-color: white;
  margin: 0 0.4rem 0 0;
  font-size: 1.3rem;
  border-radius: 0.1rem;
  position: relative;
  .fab {
    position: absolute;
    top: 0.3rem;
    left: 0.5rem;

  }
}


.menu-icon {
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
