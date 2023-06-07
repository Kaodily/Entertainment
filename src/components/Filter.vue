<template>
  <div class="search_container">
    <div>
      <img src="../../public/assets/icon-search.svg" alt="" />
    </div>
    <input type="text" placeholder="Search for movies or TV series" />
  </div>
</template>
<script setup></script>
<style scoped>
.search_container {
  display: flex;
  width: 100%;
  height: max-content;
  align-items: center;
  padding: 10px 20px;
  margin-top: 15px;
}
input {
  width: 100%;
  background-color: inherit;
  border: none;
  margin-left: 10px;
  padding: 10px 20px;
}
</style>
