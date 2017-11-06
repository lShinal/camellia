<template>
  <input class="search-bar__input-field" type="search" title="Search" placeholder="Filter bookmarks or press Enter to search Google">
</template>

<script>
  export default {
    name: 'SearchBar',
  };
</script>

<style scoped>
  .search-bar__input-field {
    padding: .5rem;
    border-radius: 4px;
    background-color: rgba(255,255,255,.3);
    width: calc(100% - (var(--search-bar-margin) * 2));
    transition: .5s background-color;
  }

  .search-bar__input-field:hover {
    background-color: rgba(255,255,255,.4);
    transition: .5s background-color;
  }

  .search-bar__input-field:focus,
  .search-bar__input-field:active {
    background-color: rgba(255,255,255,.6);
    transition: .5s background-color;
  }

  .search-bar__input-field::placeholder {
    color: rgba(255,255,255,.6);
    transition: .5s color;
  }

  .search-bar__input-field:focus::placeholder,
  .search-bar__input-field:active::placeholder {
    color: transparent;
    transition: .5s color;
  }
</style>
