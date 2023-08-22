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
            ],
        };
    },
};
</script>

<template>
    <header>
        <img src="../assets/img/dc-logo.png" alt="">
        <ul>
            <li v-for="link in navLinks">
                <a href="#" :class="{ active: link.name === 'COMICS' }">
                    {{ link.name }}
                </a>
            </li>
        </ul>
    </header>
</template>

<style scoped></style>