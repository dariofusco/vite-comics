<script>
export default {
    data() {
        return {
            navLinks: [
                { name: "CHARACTERS" },
                { name: "COMICS" },
                { name: "MOVIES" },
                { name: "TV" },
                { name: "GAMES" },
                { name: "COLLECTIBLES" },
                { name: "VIDEOS" },
                { name: "FANS" },
                { name: "NEWS" },
                { name: "SHOP"},
            ],
        };
    },
};
</script>

<template>
    <header>
        <div class="container d-flex justify-content-between align-items-center py-2">
            <img src="../assets/img/dc-logo.png" alt="">
            <ul class="nav nav-pills d-flex list-unstyled">
                <li class="nav-item" v-for="link in navLinks">
                    <a href="#" class="nav-link" :class="{ active: link.name === 'COMICS' }">
                        {{ link.name }}
                    </a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
.nav-link {
    color: black;
}
.active {
    color: #0076e5;
    background-color: white;
    border-bottom: 3px solid #0076e5;
    border-radius: 0;
}
</style>