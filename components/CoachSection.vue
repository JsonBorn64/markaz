<template>
    <section class="coach-section">
        <img class="flower" src="assets/images/flower.svg" alt="flower">
        <img class="flower2" src="assets/images/flower.svg" alt="flower">
        <h2>Наши преподаватели</h2>
        <div class="coaches">
            <div class="coach">
                <img src="assets/images/Stasia.png" alt="Stasia">
                <div class="name">Муаллима<br> Стася</div>
            </div>
            <div class="coach">
                <img src="assets/images/Aysha.png" alt="Aysha">
                <div class="name">Муаллима<br> Айша</div>
            </div>
            <div class="coach">
                <img src="assets/images/Uslyam.png" alt="Isliam">
                <div class="name">Муаллима<br> Умм Ислям</div>
            </div>
        </div>
        <div class="tip">*Нажмите на картинку, чтобы увидеть информацию о преподавателях.*</div>
        <img src="assets/images/curve-lines.svg" alt="lines" class="curve-lines">
    </section>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.coach-section {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    height: 100vh;
    box-sizing: border-box;
    padding: 1em 0;

    >h2 {
        font-size: calc(var(--ratio) * 2);
        letter-spacing: 0.07em;
        text-align: center;
        // margin: 0.8em 0 1em;
        margin: 0;
    }

    >.coaches {
        display: flex;
        width: 100%;
        max-width: calc(var(--ratio) * 41.2);

        >.coach {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 33.32%;
            cursor: pointer;

            >img {
                width: 100%;
            }

            >.name {
                font-family: "SnellBT", sans-serif;
                font-size: calc(var(--ratio) * 1.4);
                text-align: center;
                margin-top: calc(var(--ratio) * 0.8);
            }
        }
    }

    >.tip {
        font-size: calc(var(--ratio) * 0.8);
        // margin-top: 3em;
    }

    >.flower {
        position: absolute;
        top: -32%;
        left: -12%;
        width: calc(var(--ratio) * 31.4);
        animation: flower 200s infinite;

        @keyframes flower {
            0% {
                transform: rotate(0);
            }
            100% {
                transform: rotate(360deg);
            }
        }
    }

    >.flower2 {
        position: absolute;
        bottom: -26%;
        right: -18%;
        width: calc(var(--ratio) * 31.4);
        animation: flower 200s infinite;

        @keyframes flower {
            0% {
                transform: rotate(0);
            }
            100% {
                transform: rotate(360deg);
            }
        }
    }

    >.curve-lines {
        width: calc(var(--ratio) * 31.5);
    }
}
</style>