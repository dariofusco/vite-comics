<script>
export default {
    data() {
        return {
            footerLinksComics: [
                { name: "Characters" },
                { name: "Comics" },
                { name: "Movies" },
                { name: "TV" },
                { name: "Games" },
                { name: "Videos" },
                { name: "News" },
            ],
            footerLinksShop: [
                { name: "Shop DC" },
                { name: "Shop DC Collectibles" },
            ],
            footerLinksDc: [
                { name: "Therms Of Use" },
                { name: "Privacy policy (New)" },
                { name: "Ad Choises" },
                { name: "Advertising" },
                { name: "Jobs" },
                { name: "Subscriptions" },
                { name: "Talent Workshops" },
                { name: "CPSC Certificates" },
                { name: "Ratings" },
                { name: "Shop Help" },
                { name: "Contact Us" },
            ],
            footerLinksSites: [
                { name: "DC" },
                { name: "MAD Magazine" },
                { name: "DC Kids" },
                { name: "DC Universe" },
                { name: "DC Power Visa" },
            ],
        };
    },
};
</script>

<template>
    <footer>
        <div class="container d-flex">
            <div class="py-3">
                <h4>DC COMICS</h4>
                <ul class="list-unstyled">
                    <li v-for="link in footerLinksComics"><a href="#">{{ link.name }}</a></li>
                </ul>
                <h4>SHOP</h4>
                <ul class="list-unstyled">
                    <li v-for="link in footerLinksShop"><a href="#">{{ link.name }}</a></li>
                </ul>
            </div>

            <div class="py-3 px-5">
                <h4>DC</h4>
                <ul class="list-unstyled">
                    <li v-for="link in footerLinksDc"><a href="#">{{ link.name }}</a></li>
                </ul>
            </div>

            <div class="py-3">
                <h4>SITES</h4>
                <ul class="list-unstyled">
                    <li v-for="link in footerLinksSites"><a href="#">{{ link.name }}</a></li>
                </ul>
            </div>

        </div>
    </footer>
    <div class="grey-background">
        <div class="container d-flex justify-content-between align-items-center py-4">
            <button type="button" class="btn btn-outline-primary">SIGN-UP NOW!</button>
            <div>
                <span class="px-4">FOLLOW US</span>
                <img class="px-1" src="../assets/img/footer-facebook.png" alt="">
                <img class="px-1" src="../assets/img/footer-twitter.png" alt="">
                <img class="px-1" src="../assets/img/footer-youtube.png" alt="">
                <img class="px-1" src="../assets/img/footer-pinterest.png" alt="">
                <img class="px-1" src="../assets/img/footer-periscope.png" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
footer {
    background-image: url(../assets/img/footer-bg.jpg);
}

h4 {
    color: white;
}

a {
    text-decoration: none;
    color: #7c7d7d;
}

.grey-background {
    background-color: #2c2c2c;
}

span {
    color: #0076e5;
}

.btn {
    color: white;
    border-radius: 0;
}
</style>