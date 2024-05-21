<template>
    <header>
        <nav class="nav">
            <div class="container">
                <div class="nav__content">
                    <a href="#" class="logo">VUE ROUTER</a>
                    <ul class="nav__list">
                        <li v-for="link in links" :key="link.title">
                            <router-link class="nav__link" :to="link.url">
                                {{ link.title }}
                            </router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    props: {
        links: {
            typeof: Array,
            default: [],
        },
    },
};
</script>

<style>
* {
    padding: 0;
    margin: 0;
    list-style: none;
    text-decoration: none;
    box-sizing: border-box;
}

.container {
    max-width: 1140px;
    width: 100%;
    margin: 0 auto;
}

.nav {
    padding: 20px 0;
    background: #d1d1d1;
}

.nav__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav__list {
    display: flex;
    align-items: center;
    gap: 30px;
}

.nav__link {
    font-size: 18px;
}
</style>
