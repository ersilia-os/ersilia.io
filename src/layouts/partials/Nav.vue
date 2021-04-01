<template>
  <nav class="main-nav flex gap-15">

    <g-link to="/">
      <span class="main-nav__label">Home</span>
    </g-link>

    <g-link to="/soon/">
      <span class="main-nav__label">Models</span>
    </g-link>

    <g-link to="/docs/">
      <span class="main-nav__label">Docs</span>
    </g-link>

    <g-link to="/blog/">
      <span class="main-nav__label">Blog</span>
    </g-link>

  </nav>
</template>


<style lang="scss">
.main-nav {
  flex-wrap: nowrap;
}
@media screen and (max-width: 850px) {
 .main-nav {
    order: 10;
    min-width: 100%;
    a {
      padding-top: 5px;
      padding-bottom: 10px;
    }
  }
}
</style>
