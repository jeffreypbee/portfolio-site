<template>
  <div id="app">
    <header class="middle-gradient">
      <div id="site-name">
        jeffrey<span class="red-text">p</span><span class="blue-text">bee</span><span class="red-text">.</span>com
      </div>      
      <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
      </nav>
    </header>
    
    <main>
      <router-view/>
    </main>
    
    <footer class="middle-gradient">
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
  background-color: rgba(50, 50, 50, 0.2);
  animation: translucentbg 15s ease infinite;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #eee;
  height: 100%;
  display: grid;
  grid-template-rows: 10% auto 5%;
  grid-template-areas: "header"
                      "body"
                      "footer";
}

@keyframes translucentbg {
  20% {
    background-color: rgba(50, 50, 50, 0.4);
  }
  50% {
    background-color: rgba(50, 50, 50, 0.6);
  }
  70% {
    background-color: rgba(50, 50, 50, 0.4);
  }
  100% {
    background-color: rgba(50, 50, 50, 0.2);
  }
  
}

header {
  grid-area: header;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  padding: 10px;
  padding-bottom: 0px;
  border-bottom: 1px solid white;
}

body {
  grid-area: body;
}

footer {
  grid-area: footer;
  display: flex;
  flex-direction: column;
  justify-content: center;
  border-top: 1px solid white;
}

.middle-gradient {
  background: linear-gradient(to right, rgba(50, 50, 50, 0), rgba(50, 50, 50, .5), rgba(50, 50, 50, 0));
}

#site-name {
  font-weight: bold;
  font-size: 2rem;
  text-shadow: 2px 2px 1px rgba(0, 0, 0, 0.3);
  padding: 10px;
}

a {
  font-weight: bold;
  color: var(--blue);
  text-decoration: none;
}

nav {
  padding-bottom: 0px;
}

nav a {
  padding: 5px;
  padding-bottom: 1px;
  margin-bottom: 0px;
  margin-right: 5px;
  color: var(--darkgray);
  background-color: var(--lightgray);
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

nav a.router-link-exact-active {  
  color: var(--darkgray);
  background-color: white;
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
