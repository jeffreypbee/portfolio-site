<template>
  <div id="app">
    <header>
      <div id="site-name">
        jeffrey<span class="red-text">p</span><span class="blue-text">bee</span><span class="red-text">.</span>com
      </div>      
      <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </nav>
    </header>
    
    <main>
      <router-view/>
    </main>
    
    <footer>
      Copyright &copy; 2023 Jeffrey Bee
    </footer>
  </div>
</template>

<style>
:root {
  --red: red;
  --blue: #0099ff;
  --lightgray: lightgray;
  --darkgray: #333;
}

body {
  background: linear-gradient(-45deg, var(--red), var(--blue));
  background-size: 400% 400%;
  height: 100vh;
  margin: 0px;
  padding: 0px;
  animation: gradient 15s ease infinite;
}

@keyframes gradient {
  0% {
		background-position: 0% 50%;
	}
	50% {
		background-position: 100% 50%;
	}
	100% {
		background-position: 0% 50%;
	}
}

#app {
  background-color: rgba(50, 50, 50, 0.6);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #eee;
  height: 100%;
  display: grid;
  grid-template-rows: 20% auto 20%;
  grid-template-areas: "header"
                      "body"
                      "footer";
}

header {
  grid-area: header;
  display: flex;
  justify-content: space-between;
}

body {
  grid-area: body;
}

footer {
  grid-area: footer;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
}

#site-name {
  font-weight: bold;
  font-size: 2rem;
  text-shadow: 2px 2px 1px rgba(0, 0, 0, 0.3);
}

a {
  font-weight: bold;
  color: var(--blue);
}

nav a {
  border-radius: 10px;
  padding: 5px;
}

nav a.router-link-exact-active {  
  color: white;
}

.red-text {
  color: var(--red);
}

.blue-text {
  color: var(--blue);
}

.light-gray-text {
  color: var(--lightgray);
}
</style>
