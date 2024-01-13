<template>
    <section class="about-section">
        <div class="center">
            <h2>Марказ An-Nur - <br>проводник в мир<br> Корана!</h2>
            <p>Мы обучаем чтению Корана и его заучиванию. Учить Коран для начинающих дело непростое, требующее усердия для изучающего, Аллах облегчает, а наш марказ помогает в реализации этой цели и поддерживает своих учениц на протяжении всего пути.</p>
        </div>
        <img src="assets/images/flower.svg" alt="flower">
    </section>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.about-section {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;

    >.center {
        position: relative;
        width: 100%;
        max-width: calc(var(--ratio) * 41.2);
        height: calc(var(--ratio) * 17.6);
        border: 1px solid var(--brown);
        border-radius: 0 calc(var(--ratio) * 3);

        >h2 {
            position: absolute;
            left: -1px;
            top: 0;
            margin: 0;
            padding: calc(var(--ratio) * 1) 0 calc(var(--ratio) * 5);
            font-size: calc(var(--ratio) * 2);
            max-width: calc(var(--ratio) * 15);
            line-height: calc(var(--ratio) * 1.8);
            white-space: nowrap;
            border-left: 1px solid var(--background);
        }

        >p {
            position: absolute;
            right: -1px;
            bottom: 0;
            margin: 0;
            padding: calc(var(--ratio) * 5) 0 calc(var(--ratio) * 1);
            border-right: 1px solid var(--background);
            max-width: calc(var(--ratio) * 22.92);
            font-size: calc(var(--ratio) * 0.8);
            letter-spacing: 4%;
            line-height: calc(var(--ratio) * 1.1);
            text-align: justify;
        }
    }

    >img {
        position: absolute;
        top: -27%;
        left: -7%;
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