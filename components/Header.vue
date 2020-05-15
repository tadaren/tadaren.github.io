<template>
  <b-navbar>
    <template slot="brand">
      <b-navbar-item to="/" tag="nuxt-link">
        Tadaren
      </b-navbar-item>
    </template>

    <template slot="end">
      <b-navbar-item to="/" tag="nuxt-link">
        Home
      </b-navbar-item>
      <b-navbar-item to="/about" tag="nuxt-link">
        About
      </b-navbar-item>
      <b-navbar-item to="/works" tag="nuxt-link">
        Works
      </b-navbar-item>
      <b-navbar-item to="/contact" tag="nuxt-link">
        Contact
      </b-navbar-item>
    </template>
  </b-navbar>
</template>
