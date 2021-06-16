<template>
  <div>
    <div data-collapse="medium" data-animation="default" data-duration="400" role="banner" class="w-nav">
      <div class="w-container">
        <nuxt-link to="/" class="w-nav-brand">
          <div class="text-block">Hello Oonops !</div>
        </nuxt-link>
        <nav role="navigation" class="w-nav-menu">
          <nuxt-link to="/" class="w-nav-link">Home</nuxt-link>
          <nuxt-link to="/api" class="w-nav-link">Api</nuxt-link>
        </nav>
        <div class="w-nav-button">
          <div class="w-icon-nav-menu"></div>
        </div>
      </div>
    </div>
    <Nuxt />
  </div>
</template>

