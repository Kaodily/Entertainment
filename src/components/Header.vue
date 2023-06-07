<script></script>

<template>
  <header>
    <div>
      <img src="../../public/assets/logo.svg" alt="logo" />
    </div>
    <div>
      <img src="../../public/assets/icon-nav-home.svg" alt="" />
      <img src="../../public/assets/icon-nav-movies.svg" alt="" />
      <img src="../../public/assets/icon-nav-tv-series.svg" alt="" />
      <img src="../../public/assets/icon-nav-bookmark.svg" alt="" />
    </div>
    <div>
      <img
        class="avatar"
        src="../../public/assets/image-avatar.png"
        width="35"
        alt="" />
    </div>
  </header>
</template>

<style scoped>
header {
  height: max-content;
  background-color: #161d2f;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 20px 0;
}
img {
  color: white;
  margin: 0 10px;
}
.avatar {
  border: 2px solid white;
  border-radius: 50%;
}
</style>
