<template>
    <div class="profile__container">
        <p class="profile__title">Привет: {{user.username}}!</p>
        <p class="profile__beer">Твоё пиво</p>
        <!--        <Profile v-for="(beer, i) of beers"-->
        <!--                 v-bind:beer="beer"-->
        <!--                 v-bind:index="i"-->
        <!--        />-->
        <Profile v-bind:beer="beers"/>
        <button class="profile__refresh-btn" v-on:click="refresh">Обновить</button>
        <router-link class="profile__home-btn" to="/">Домой</router-link>

    </div>
</template>

<script>
    import Profile from "./../components/Profile";

    export default {
        name: 'profile',
        mounted() {
            fetch('https://random-data-api.com/api/beer/random_beer')
                .then(response => response.json())
                .then(json => {
                    this.beers = json
                })
            fetch('https://random-data-api.com/api/users/random_user')
                .then(response => response.json())
                .then(json => {
                    this.user = json
                })

        },
        methods: {
            refresh() {
                fetch('https://random-data-api.com/api/beer/random_beer')
                    .then(response => response.json())
                    .then(json => {
                        this.beers = json
                    })
            }
        },
        data() {
            return {
                user: {},
                beers: {}
            }
        },
        components: {
            Profile,

        }
    }

</script>

<style scoped>
    .profile__beer {
        margin: 40px 0 20px 0;
        font-size: 20px;
        border-bottom: 1px solid slategray;
        max-width: 1280px;
        width: 100%;
        text-align: center;
        padding-bottom: 10px;
    }

    .profile__title {
        margin: 20px 0 0 0;
        font-size: 30px;
    }

    .profile__container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .profile__home-btn {
        max-width: 1280px;
        width: 100%;
        height: 50px;
        text-align: center;
        border: #323232 1px solid;
        background-color: #b8bb65;
        text-decoration: none;
        color: black;
        font-size: 2rem;
        transition: .5s linear;
    }

    .profile__refresh-btn {
        max-width: 1280px;
        width: 100%;
        height: 50px;
        text-align: center;
        border: #323232 1px solid;
        background-color: #6a6a67;
        text-decoration: none;
        color: black;
        font-size: 2rem;
        margin-bottom: 10px;
        cursor: pointer;
        transition: .5s linear;
    }
    .profile__refresh-btn:hover{
        opacity: .5;
    }
    .profile__home-btn:hover{
        opacity: .5;
    }
    @media screen and (max-width: 320px) {
        .profile__refresh-btn, .profile__home-btn {
            max-width: 320px;
            height: 30px;
            color: black;
            font-size: 1rem;
            margin-bottom: 5px;
        }

        .profile__beer {
            margin: 20px 0 10px 0;
            font-size: 14px;
            border-bottom: 1px solid slategray;
            max-width: 320px;
            width: 100%;
            text-align: center;
            padding-bottom: 5px;
        }

        .profile__title {
            margin: 10px 0 0 0;
            font-size: 15px;
        }

    }
</style>
