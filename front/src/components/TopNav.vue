<template>
  <main>
    <div id="left">
      <router-link to="/">Home</router-link>
      <router-link>link 1</router-link>
      <router-link>Link 2</router-link>
      <router-link to="">Link 4</router-link>
    </div>

    <div id="right">
      <router-link>Login</router-link>
      <router-link>Sign Up</router-link>
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f0f0f0;
  position: sticky;
  top: 0;
  padding: 0.5%;
  width: 100%;
  box-shadow: var(--shadow);
}

#right {
  margin-left: auto;
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  padding: 0 10px;
}

#left {
  margin-right: auto;
  display: flex;
  justify-content: space-between;
  padding: 0 10px;
}

#left a {
  position: relative;
  margin: 0 5px;
}

#left a::after {
  content: '';
  position: absolute;
  bottom: 0%;
  left: 0;
  width: 0%;
  height: 2px;
  background-color: var(--primary);
}

#left a:hover::after {
  width: 100%;
}

#right a,
#left a {
  padding: 5px;
}

#right a {
  border: 1px solid var(--primary);
}

#right a:hover {
  background-color: var(--hover);
  border-color: var(--hover);
}

#right a:first-child {
  color: var(--primary);
}

#right a:first-child:hover {
  color: var(--white);
}

#right a:last-child {
  background-color: var(--primary);
  color: var(--white);
}
</style>
