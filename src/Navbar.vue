<template>
    <nav class="main-nav">
        <h1>Menu</h1>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
</template>

<script>
export default {
   name: 'Navbar',
   data() {
       return {

       }
   } 
}
</script>

<style scooped>

nav {
    text-align: center;
}

nav li {
    display: inline-block;
    list-style-type: none;
    margin: 0;
}

ul{
    padding: 0;
}
</style>