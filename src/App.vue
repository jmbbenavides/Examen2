<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/registro">Registro</router-link>
    </nav>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0;
  padding: 0;
}

nav {
  padding: 20px 30px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  text-align: center;
}

nav a {
  font-weight: 600;
  color: white;
  text-decoration: none;
  margin: 0 15px;
  padding: 10px 20px;
  border-radius: 25px;
  transition: all 0.3s ease;
  display: inline-block;
  font-size: 16px;
}

nav a:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-2px);
}

nav a.router-link-exact-active {
  background: rgba(255, 255, 255, 0.25);
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

/* Responsive navigation */
@media (max-width: 600px) {
  nav {
    padding: 15px;
  }
  
  nav a {
    display: block;
    margin: 5px 0;
    font-size: 14px;
  }
}
</style>
