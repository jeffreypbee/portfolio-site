<template>
  <div id="app">
    <header>
      <div id="site-name">
        jeffrey<span class="gray-text">p</span>bee<span class="gray-text">.com</span>
      </div>      
      <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/projects">Projects</router-link>
        <router-link to="/about">About</router-link>
      </nav>
    </header>
    
    <main class="middle-gradient">
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
  --gray: #aaa;
  --darkgray: #333;
}

body {
  background: linear-gradient(15deg, var(--red), var(--blue));
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
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
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
  border-bottom: 3px solid white;
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
  color: var(--gray);
  background-color: #3335
}

.middle-gradient {
  background: linear-gradient(to right, rgba(50, 50, 50, .5), rgba(50, 50, 50, .8), rgba(50, 50, 50, .5));
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
  position: relative;
}

nav a {
  position: relative;
  top: 10px;
  padding: 5px;
  margin: 0 5px;
  color: var(--darkgray);
  background-color: var(--gray);  
  z-index: 5;
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

.gray-text {
  color: var(--gray);
}

.light-gray-text {
  color: var(--lightgray);
}

.hover-grow {
  transition: scale 1s;
}

.hover-grow:hover {
  scale: 110%;
  cursor: pointer;
}
</style>
