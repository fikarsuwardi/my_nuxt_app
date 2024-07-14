<template>
    <div>
      <nav>
        <NuxtLink to="/">Beranda</NuxtLink>
        <NuxtLink to="/about">Tentang</NuxtLink>
      </nav>
      <Nuxt />
    </div>
  </template>
  
  <style scoped>
  nav {
    background: #333;
    padding: 10px;
  }
  nav a {
    color: white;
    margin: 0 10px;
    text-decoration: none;
  }
  </style>
  