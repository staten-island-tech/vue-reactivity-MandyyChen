<template>
  <header class="header">
    <div class="logo-wrapper">
      <img alt="Vue logo" class="logo" src="@/assets/nekologo.svg" width="125" height="125" />
    </div>
    <div class="title-wrapper">
      <h1> Cat Collecter</h1>
    </div>
    <nav class="wrapper">
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/item">Item</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped>
.header {
  line-height: 1.5;
  max-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo-wrapper {
  margin-bottom: 0rem;
}

.title-wrapper {
  margin-bottom: 1rem; 
}

.wrapper {
  display: flex;
  justify-content: center;
  margin-bottom: 2rem;
}

h1 {
  font-weight: bold;
  font-size: 43px;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

.wrapper {
  width: 100%;
  font-size: 20px;
  text-align: center;
  margin-top: 2rem;
}

.wrapper a.router-link-exact-active {
  color: var(--color-text);
}

.wrapper a.router-link-exact-active:hover {
  background-color: transparent;
}

.wrapper a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

.wrapper a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  .header {
    flex-direction: row;
    justify-content: space-between;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo-wrapper {
    margin-bottom: 0; 
  }

  .title-wrapper {
    margin-bottom: 0; 
  }

  .wrapper {
    margin-top: 0; 
  }

  .wrapper {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;
    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>

