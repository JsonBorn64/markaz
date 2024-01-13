<template>
    <section class="hero-section">
        <div class="hero-img_wrap">
            <img class="hero-img" src="assets/images/hero-img.jpg" alt="hero">
            <div class="gradient"></div>
        </div>
        <img class="flower" src="assets/images/flower.svg" alt="flower">
        <div class="center">
            <header class="header">
                <nav class="menu">
                    <a href="#">О нас</a>
                    <img src="assets/images/menu-romb.svg" alt=".">
                    <a href="#">Курсы</a>
                    <img src="assets/images/menu-romb.svg" alt=".">
                    <a href="#">Учителя</a>
                    <img src="assets/images/menu-romb.svg" alt=".">
                    <a href="#">Отзывы</a>
                    <img src="assets/images/menu-romb.svg" alt=".">
                    <a href="#">Контакты</a>
                </nav>
            </header>
            <div class="hero-text">
                <h1>Онлайн-школа</h1>
                <h1>для девушек</h1>
                <div>Наша цель - помочь сёстрам стать ближе к Корану, заслужить довольство Всевышнего Аллаха, <br>
                    приблизиться к Нему своим сердцем и мыслями.</div>
                <img src="assets/images/gradient-ellipse.svg" alt="ellipse">
            </div>
            <div class="btns">
                <button class="btn">Выбрать курс</button>
                <button class="btn">Таджвид</button>
                <button class="btn">Тасхих</button>
                <button class="btn">Хифз</button>
            </div>
        </div>
    </section>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.hero-section {
    position: relative;
    display: flex;
    justify-content: center;
    width: 100%;
    height: 100vh;

    >.center {
        width: 100%;
        max-width: calc(var(--ratio) * 41.2);
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        z-index: 1;

        >.header {
            width: 100%;
            margin-top: calc(var(--ratio) * 1.6);

            >.menu {
                display: flex;
                justify-content: space-between;
                width: 100%;
                max-width: calc(var(--ratio) * 24.08);
                margin-left: auto;

                >a {
                    text-decoration: none;
                    font-size: calc(var(--ratio) * 0.8);
                    color: var(--brown);
                }

                >img {
                    width: calc(var(--ratio) * 0.4);
                }
            }
        }

        >.hero-text {
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            align-self: flex-end;

            >h1 {
                font-size: calc(var(--ratio) * 3.76);
                letter-spacing: 0.022em;
                margin: 0;
                text-shadow: 1px 1px 15px rgba(0, 0, 0, 0.15);
                background: linear-gradient(270deg, #492C1D 34%, #816659 75.52%);
                background-clip: text;
                -webkit-text-fill-color: transparent;
            }

            >h1:first-child {
                background: linear-gradient(270deg, #492C1D 3.23%, #816659 39.14%, #492C1D 75.06%);
                background-clip: text;
                -webkit-text-fill-color: transparent;
                margin-right: calc(var(--ratio) * 5.8);
                margin-bottom: calc(var(--ratio) * -0.6);
            }

            >div {
                margin-top: calc(var(--ratio) * 0.6);
                letter-spacing: 0.01em;
                max-width: calc(var(--ratio) * 23.6);
                font-size: calc(var(--ratio) * 0.8);
            }

            >img {
                position: absolute;
                top: -65%;
                left: 20%;
                width: calc(var(--ratio) * 14);
                animation: ellipse 10s infinite;

                @keyframes ellipse {
                    0% {
                        left: 10%;
                    }
                    50% {
                        left: 30%;
                    }
                    100% {
                        left: 10%;
                    }
                }
            }
        }

        >.btns {
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            width: 100%;
            margin-bottom: calc(var(--ratio) * 1.6);

            >button {
                border: 1px solid var(--brown);
                border-radius: calc(var(--ratio) * 0.8);
                padding: 0 calc(var(--ratio) * 0.65) 0 calc(var(--ratio) * 0.55);
                font-family: "SnellBT", sans-serif;
                font-size: calc(var(--ratio) * 1.4);
                height: calc(var(--ratio) * 2.12);
                background: none;
                cursor: pointer;
            }

            >.btn:first-child {
                padding: 0;
                box-shadow: 1px 1px 15px 0px rgba(0, 0, 0, 0.15);
                background: linear-gradient(274.42deg, #492C1D 3.19%, #816659 43.26%, #492C1D 83.82%);
                color: var(--background);
                font-family: "AlegreyaSC", sans-serif;
                border: none;
                font-size: calc(var(--ratio) * 1.28);
                height: calc(var(--ratio) * 2.88);
                width: calc(var(--ratio) * 10.68);
            }
        }

    }

    >.hero-img_wrap {
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        overflow: hidden;

        >.hero-img {
            height: 100%;
        }

        >.gradient {
            position: absolute;
            background: linear-gradient(90deg, rgba(255, 255, 255, 0) 0%, var(--background) 60%);
            width: 120%;
            height: 100%;
            top: 0;
            left: 0;
            transform: translateX(18%);
            animation: gradient 6s;

            @keyframes gradient {
                0% {
                    transform: translateX(-15%);
                }
                100% {
                    transform: translateX(18%);
                }
            }
        }
    }

    >.flower {
        position: absolute;
        top: -17%;
        right: -15%;
        width: calc(var(--ratio) * 31.4);
        animation: rotation 200s infinite linear;

        @keyframes rotation {
            0% {
                transform: rotate(0);
            }

            100% {
                transform: rotate(360deg);
            }
        }
    }

}
</style>