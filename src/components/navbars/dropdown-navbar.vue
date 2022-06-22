<template>
    <nav>
        <h1 id="logo">lively</h1>
        <div class="dropdown">
            <span class="bar"></span>
            <span class="bar"></span>
            <span class="bar"></span>
        </div>

        <ul>
            <li><a href="">Documentation</a></li>
            <li><a href="">Download</a></li>
            <li><a href="">Forum</a></li>
            <li><a href="">Resources</a></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name : 'dropdown-navbar',
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Lato&family=Montserrat&display=swap');

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background: rgb(13, 209, 144);
        padding: 13px;
    }

    #logo {
        font : 1.2rem 'Lato', sans-serif;
        text-transform: uppercase;
        margin: 0 0 0 10px;
        cursor: pointer;
        color:  #fff;
    }

    ul {
        display: none;
        list-style-type: none;
    }

    li {
        margin: 0 10px;
    }

    a {
        text-decoration: none;
        color: #fff;
        font: 1rem 'Montserrat', sans-serif;
    }

    a:hover {
        text-decoration: underline;
    }

    .dropdown {
        display: none;
        flex-direction: column;
        cursor: pointer;
        margin: 0 15px 0 0;
    }

    .bar {
        background: #fff;
        margin: 3px 0;
        padding: 3px;
        width: 35px;
        border-radius: 30px;
    }

        /* Extra small devices (phones, 600px and down) */
    @media only screen and (max-width: 600px) {
        .dropdown {
            display: flex;
        }
    }

</style>