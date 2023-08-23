<script>

export default {
    props: {
        imgSrc: String,
        comicsType: String,
    },
};

</script>

<template>
<div class="card">
    <img class="card-img-top" :src="imgSrc" alt="">
    <div class="card-body">
        <p class="card-text">{{ comicsType }}</p>
    </div>
</div>
</template>

<style lang="scss" scoped>
.card {
    border: 0;
    width: fit-content;
    background-color: #1c1c1c;
}
.card-img-top {
    height: 170px;
    width: 170px;
}

.card-text {
    color: white;
}
</style>