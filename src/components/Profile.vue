<template>
    <div class="profile">
        <p class="profile__text">Бренд: <span class="profile__text_underline">{{beer.brand}}</span></p>
        <p class="profile__text">Название: <span class="profile__text_underline">{{beer.name}}</span></p>
        <p class="profile__text">Солод: <span class="profile__text_underline">{{beer.malts}}</span></p>
        <p class="profile__text">Стиль: <span class="profile__text_underline">{{beer.style}}</span></p>
    </div>
</template>
<script>

    export default {
        props: {
            beer: {
                type: Object,
                required:true
            },

        },
        name: "Profile"
    }
</script>

<style scoped>
    .profile__text_underline{
        text-align: center;
        text-decoration: underline;
    }
    .profile {
        display: flex;
        flex-flow: column nowrap;
        justify-content: space-around;
        margin-bottom: 30px;
    }
    .profile__text {
        width: 100%;
        text-align: center;
        font-size: 30px;
    }
    @media screen and (max-width: 320px) {
        .profile {
            margin-bottom: 10px;
        }

        .profile__text {
            width: 100%;
            text-align: center;
            font-size: 15px;
        }
    }

</style>
