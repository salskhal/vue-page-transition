<template>
    <nav>
        <ul>
            <router-link to="/">
                <li>Home</li>
            </router-link>
            <router-link to="/contact">
                <li>Contact</li>
            </router-link>
        </ul>
    </nav>
</template>

<style scoped>
nav{
    font-size: 1.5rem;
    font-weight: 500;
    position: relative;
    z-index: 20;
}
ul{
    display: flex;
    gap: 3rem;
    list-style: none;
}

nav a{
    text-decoration: none;
    color: black;
}

nav a.router-link-exact-active {
  text-decoration: underline;
  color: brown;
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}
</style>