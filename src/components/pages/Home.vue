<script>
import { mapGetters } from "vuex"

import Slider from "../shared/Slider.vue"

export default {
    created() {
        this.$store.dispatch("popularMovies")
        this.$store.dispatch("trendMovies")
    },
    components: {
        Slider,
    },
    computed: {
        ...mapGetters(["getPopularMovies", "getTrendMovies"]),
    },
}
</script>

<template>
    <div class="container">
        <div class="home">
            <Slider title="Popular Movies" :movies="getPopularMovies" />
            <Slider title="Trend Movies" :movies="getTrendMovies" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    display: flex;
    justify-content: center;
    background-color: rgb(255, 255, 255);

    .home {
        width: 60%;
    }
}
</style>
