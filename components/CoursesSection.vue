<template>
    <section class="courses-section">
        <h2>Курсы</h2>
        <div class="center">
            <div class="card" :class="{second: courseNum == 1, third: courseNum == 2}" :style="{zIndex: courseNum == 1 ? 1 : ''}">
                <div class="title">Хифз</div>
                <p>Курс для тех, кто хочет<br> <span>выучить Коран наизусть.</span></p>
                <div class="line"></div>
                <p class="bold">Краткое описание:</p>
                <p class="decore">Проверка заученного<br> объема<br> с исправлением ошибок<br> при чтении. <br>
                    Помощь в повторении выученного объема.</p>
                <div class="line"></div>
                <p class="bold">Длительность курса:</p>
                <p class="decore">Индивидуально.</p>
                <div class="line"></div>
                <p>Групповые - <span>2000</span>₽ \мес.
                    Индивидуальные - <span>4000</span>₽ \мес.</p>
                <div class="confirm-btn">Выбрать</div>
            </div>
            <div class="left-btn" @click="nextCourse()">
                <img src="assets/images/arrow.svg" alt="<">
            </div>
            <div class="card" :class="{second: courseNum == 2, third: courseNum == 3}" :style="{zIndex: courseNum == 2 ? 1 : ''}">
                <div class="title">Таджвид</div>
                <p>Курс для тех, кто хочет<br> <span>выучить Коран с 0.</span></p>
                <div class="line"></div>
                <p class="bold">Краткое описание:</p>
                <p class="decore">Правильная постановка<br>махраджа, разбор всех <br> правил таджвида, тасхих.</p>
                <p class="decore">В большей части курс практический, что <br>позволяет лучше усваивать информацию и сразу же оттачивать правила на<br> практике.</p>
                <div class="line"></div>
                <p class="bold">Длительность курса:</p>
                <p class="decore">3-3,5 месяца.</p>
                <div class="line"></div>
                <p>Групповые - <span>2000</span>₽ \мес.
                    Индивидуальные - <span>4000</span>₽ \мес.</p>
                <div class="confirm-btn">Выбрать</div>
            </div>
            <div class="right-btn" @click="prevCourse()">
                <img src="assets/images/arrow.svg" alt=">">
            </div>
            <div class="card" :class="{second: courseNum == 3, third: courseNum == 1}" :style="{zIndex: courseNum == 3 ? 1 : ''}">
                <div class="title">Тасхих</div>
                <p>Курс для тех, кто знает<br> алфавит и правила чтения Корана, но хотел бы<br>  <span>поработать над своими ошибками.</span></p>
                <div class="line"></div>
                <p class="bold">Краткое описание:</p>
                <p class="decore">Исправление ошибок<br> при чтении Корана<br> посредством контроля<br> учителя.</p>
                <div class="line"></div>
                <p class="bold">Длительность курса:</p>
                <p class="decore">Индивидуально.</p>
                <div class="line"></div>
                <p>Групповые - <span>2000</span>₽ \мес.
                    Индивидуальные - <span>4000</span>₽ \мес.</p>
                <div class="confirm-btn">Выбрать</div>
            </div>
        </div>
        <div class="bottom-decore">Таджвид</div>
    </section>
</template>

<script setup>
let courseNum = ref(2)

function nextCourse() {
    if (courseNum.value < 3) courseNum.value += 1
    else courseNum.value = 1
}

function prevCourse() {
    if (courseNum.value > 1) courseNum.value -= 1
    else courseNum.value = 3
}
</script>

<style lang="scss" scoped>
.courses-section {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    position: relative;
    height: 100vh;
    width: 100%;
    background: linear-gradient(90deg, #1F1914 0%, rgba(31, 25, 20, 0.5) 100%), url('assets/images/courses-img.jpg') center/cover no-repeat;

    >h2 {
        font-size: calc(var(--ratio) * 2);
        letter-spacing: 0.07em;
        text-align: center;
        color: var(--background);
        margin: 0.8em 0 1em;
    }

    >.center {
        position: relative;
        width: 100%;
        max-width: calc(var(--ratio) * 41.2);
        min-height: calc(var(--ratio) * 21);
        user-select: none;

        >.card {
            position: absolute;
            display: flex;
            flex-direction: column;
            justify-content: center;
            top: 50%;
            left: 0;
            transform: translate(0%, -50%);
            width: calc(var(--ratio) * 10.88);
            border-radius: calc(var(--ratio) * 0.8);
            height: 85%;
            opacity: 0.5;
            background: var(--background);
            padding: 0 2em;
            font-size: calc(var(--ratio) * 0.6);
            box-sizing: border-box;
            transition: 600ms;

            >.title {
                position: absolute;
                display: grid;
                place-content: center;
                color: var(--background);
                top: -6%;
                left: 8%;
                height: calc(var(--ratio) * 1.72);
                border-radius: calc(var(--ratio) * 0.48);
                padding: 0 0.45em 0 0.35em;
                font-family: "SnellBT", sans-serif;
                font-size: calc(var(--ratio) * 1.32);
                background: linear-gradient(274.42deg, #492C1D 3.19%, #816659 43.26%, #492C1D 83.82%);
                transition: 600ms;
            }

            >.line {
                background-color: rgba(73, 44, 29, 0.2);
                width: 100%;
                height: 1px;
                margin-top: calc(var(--ratio) * 0.2);
                margin-bottom: calc(var(--ratio) * 0.6);
            }

            >p {
                margin: 0;
                color: rgba(129, 102, 89, 1);
                line-height: 1.4em;

                >span {
                    color: var(--brown);
                }
            }

            >.confirm-btn {
                position: absolute;
                display: grid;
                place-content: center;
                color: var(--background);
                bottom: -3%;
                right: 5%;
                height: calc(var(--ratio) * 1.76);
                border-radius: calc(var(--ratio) * 0.48);
                padding: 0 0.45em 0 0.35em;
                font-family: "SnellBT", sans-serif;
                font-size: calc(var(--ratio) * 1.4);
                background: #DECEB2;
                color: #816659;
                cursor: pointer;
                opacity: 0;
                pointer-events: none;
                transition: 1000ms;
            }
        }

        >.second {
            left: 50%;
            font-size: calc(var(--ratio) * 0.68);
            transform: translate(-50%, -50%);
            opacity: 1;
            height: 100%;
            width: calc(var(--ratio) * 13.2);

            >.title {
                height: calc(var(--ratio) * 2.12);
                font-size: calc(var(--ratio) * 1.4);
            }

            >.confirm-btn {
                opacity: 1;
                bottom: -5%;
                pointer-events: all;
            }
        }

        >.third {
            left: 100%;
            transform: translate(-100%, -50%);
        }

        .left-btn, .right-btn {
            position: absolute;
            display: grid;
            place-content: center;
            top: 50%;
            transform: translate(0, -50%);
            width: calc(var(--ratio) * 1.6);
            height: calc(var(--ratio) * 1.6);
            cursor: pointer;
            z-index: 1;

            >img {
                width: calc(var(--ratio) * 0.4);
            }
        }

        .left-btn {
            left: 50%;
            transform: translate(-560%, -50%) rotate(180deg);
        }

        .right-btn {
            left: 50%;
            transform: translate(460%, -50%);
        }
    }

    >.bottom-decore {
        font-family: 'SnellBT', sans-serif;
        font-size: calc(var(--ratio) * 8);
        letter-spacing: 0.07em;
        color: rgba(255, 244, 238, 0.05);
        text-shadow: 0 0 calc(var(--ratio) * 2) rgba(0, 0, 0, 0.5);
        margin: -0.4em 0 -0.2em 0;
    }
}

.bold {
    font-weight: bold;
    color: var(--brown) !important;
    margin-bottom: 0.2em !important;
}

.decore {
    &::before {
        content: "";
        background-image: url('assets/images/menu-romb.svg');
        margin-right: calc(var(--ratio) * 0.2);
        display: inline-block;
        width: calc(var(--ratio) * 0.4);
        height: calc(var(--ratio) * 0.4);
        background-size: cover;
    }
}
</style>