<template>
    <div class="home">
        <h2>Главная страница</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aperiam, cum inventore non praesentium quaerat
            quasi! Deleniti fugit minima nisi numquam.</p>
        <router-link class="home__link-btn" to="/profile">Profile</router-link>
    </div>
</template>

<style scoped>
    .home {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    h2 {
        margin-top: 50px;
        margin-bottom: 50px;
    }

    p {
        margin: 15px;
        font-size: 30px;
        text-align: center;
    }

    .home__link-btn {
        max-width: 1280px;
        width: 100%;
        height: 50px;
        text-align: center;
        border: #323232 1px solid;
        background-color: #b8bb65;
        text-decoration: none;
        color: black;
        font-size: 2rem;
    }

    @media screen and (max-width: 320px) {
        h2 {
            margin-top: 20px;
            margin-bottom: 30px;
        }

        p {
            margin: 10px;
            text-align: center;
            font-size: 20px;
        }
        .home__link-btn {
            margin: 10px;
            height: 20px;
            max-width: 320px;
            font-size: 1rem;
        }
    }
</style>
