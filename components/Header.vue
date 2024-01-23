<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
      <nuxt-link to="/" class="navbar-brand">ホーム</nuxt-link>
      
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <nuxt-link  class="nav-link" to="/value">価格別</nuxt-link>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <nuxt-link  class="nav-link" to="/Maker">おすすめメーカー</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/New" class="nav-link">初心者向け</nuxt-link>
          </li>
        </ul>
        
      </div>
    </div>
  </nav>
</template>
