<template>
  <nav class="navbar">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src="Spotify_logo_without_text.svg.png" alt="" width="30" height="24">
      </a>
      <div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton1" data-bs-toggle="dropdown" aria-expanded="false">Dropdown button</button>
  <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
    <li><a class="dropdown-item" href="#">Rock</a></li>
    <li><a class="dropdown-item" href="#">Pop</a></li>
    <li><a class="dropdown-item" href="#">Jazz</a></li>
    <li><a class="dropdown-item" href="#">Metal</a></li>
  </ul>
</div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'HeaderDischi'
}
</script>

}
<style lang="scss" scoped>
img {
  width: 50px;
  height: 50px;
}
.navbar {
    margin-top: -60px;
    background-color: rgb(19%, 23%, 27%);
}

</style>
