<script>
</script>

<template>
    <div class="footer-top">
        <div class="wrapper">
            <div>
                scritte varie
            </div>
            <div class="logo">
                <img src="../assets/dc-logo-bg.png" alt="logo dc bg">
            </div>
        </div>
    </div>
    <div class="footer-bottom">
        <div class="container">
            <div class="container-button">
                <span class="button">SIGN-UP NOW!</span>
            </div>
            <div class="social">
                <span>FOLLOW US</span>
                <img src="../assets/footer-facebook.png" alt="Facebook icon">
                <img src="../assets/footer-twitter.png" alt="Twitter icon">
                <img src="../assets/footer-youtube.png" alt="Youtube icon">
                <img src="../assets/footer-pinterest.png" alt="Pinterest icon">
                <img src="../assets/footer-periscope.png" alt="Periscope icon">
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables' as*;

.footer-top {
    height: 400px;
    background-image: url(../assets/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    .wrapper {
        width: 80%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: auto;

    }

    .logo {

        img {
            width: 80%;

        }
    }
}

.footer-bottom {
    background-color: rgb(48, 48, 48);
    position: relative;
    z-index: 2;
    height: 110px;
    display: flex;


    .container {
        width: 80%;
        margin: auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .container-button {
            .button {
                padding: 10px;
                color: white;
                border: solid 2px $color-primary;
            }

        }

        .social {
            display: flex;
            align-items: center;

            span {
                color: $color-primary;
                padding: 10px;
                font-weight: bold;
            }

            img {
                padding: 10px;
            }
        }
    }
}
</style>