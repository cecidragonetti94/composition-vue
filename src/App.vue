<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>|
        <router-link to="/paises">Paises</router-link>|
     <router-link to="/cont">Cont</router-link>
  </div>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
 background-color: #f0cc95;
}

#nav {
  padding: 30px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

#nav a {
  font-weight: bold;
  color: #c78117;
  text-decoration: none;
  font-size: 30px;
}

#nav a.router-link-exact-active {
  color: #e0240b;
}
</style>
