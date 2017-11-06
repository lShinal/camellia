<template>
  <div id="app">
    <SearchBar class="app__search" />
    <BookmarkList />
  </div>
</template>

<script>
  import SearchBar from './components/SearchBar';
  import BookmarkList from './components/BookmarkList';

  export default {
    name: 'app',
    components: { SearchBar, BookmarkList },
  };
</script>

<style>
  @import "../node_modules/divine.css/src/divine.css";
  @import "variables.css";
  @import "fonts.css";

  body {
    font-family: 'Roboto', sans-serif;

    background-color: #000;
  }

  body:before {
    position: fixed;
    top: 0;
    left: 0;

    width: 100vw;
    height: 100vh;

    content: '';

    background-repeat: no-repeat no-repeat;
    background-position: center;
    background-size: cover;
    background-image: url(https://i.imgur.com/Lsnc2yC.jpg);
    opacity: 0.5;
    transition: opacity 1s ease-in-out;

    will-change: transform;

    z-index: -1;
  }

  .app__search {
    margin: var(--search-bar-margin);
  }
</style>
