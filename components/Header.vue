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
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <nuxt-link to="/info" class="nav-link">情報</nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/contact" class="nav-link">お問い合わせ</nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
