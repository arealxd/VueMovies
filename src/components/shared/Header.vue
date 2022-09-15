<script>
export default {}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <router-link to="/" tag="a">
                    <img src="../../assets/logo.png" />
                </router-link>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    height: 7rem;
    background: #11124e;
    display: flex;
    justify-content: center;

    .container {
        width: 60%;
        display: flex;
        align-items: center;

        .logo {
            cursor: pointer;
            height: 4rem;

            img {
                width: 4rem;
            }
        }
    }
}
</style>
