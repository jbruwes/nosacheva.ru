<template>
    <div ref="jarallaxRef" class="ui basic vertical fitted segment jarallax mceNonEditable  min-h-[60vh]" :style="`background-image:url(${url})`">
        <div class="ui active light dimmer">
            <div class="content"><router-link class="ui header hvr-icon-wobble-vertical massive inverted icon" style="font-family: Arsenal, sans-serif;"><i class="hvr-icon !h-28 icon mx-auto" :class="page.i"></i><span class="ui">{{ page.title }}<span class="sub header">{{
                            page.description
                        }}</span></span></router-link></div>
        </div>
    </div>
    <p>&nbsp;</p>
    <div class="ui container">
        <p style="text-align: justify;">Свой метод оздоровления, реабилитации и долголетия Наталия Григорьевна создавала
            на
            протяжении долгих лет. В далёком 1981 году, после страшной аварии, врачи приговорили Наталию Носачеву к
            пожизненной инвалидности. Но она не сдалась. Тяжёлым, кропотливым, ежедневным трудом ей удалось вернуться к
            полноценной жизни.</p>
        <p>&nbsp;</p>
        <div class="ui message">
            <div class="ui grid stackable">
                <div class="four wide column">
                    <h1 class="column" style="line-height: 75%;">20 лет+</h1>
                    <hr>
                    <p>более 20 лет Наталия Григорьевна делилась своими бесценными знаниями, позволяющими вести
                        здоровую,
                        гармоничную жизнь, справляться с заболеваниями и трудностями</p>
                </div>
                <div class="four wide column">
                    <h1 class="column" style="line-height: 75%;">&gt; 5.000</h1>
                    <hr>
                    <p>за долгие годы существования Школы обучение прошли более пяти тысяч человек, многие из них со
                        временем начали вести собственную практику в сфере оздоровительных услуг</p>
                </div>
                <div class="four wide column">
                    <h1 class="column" style="line-height: 75%;">&gt; 75%</h1>
                    <hr>
                    <p>более 75% выпускников Школы успешно решили свои проблемы и перешли на новый этап развития, они не
                        только продолжают своё саморазвитие, но и помогают родным и близким</p>
                </div>
                <div class="four wide column">
                    <h1 class="column" style="line-height: 75%;">+5 стран&nbsp;</h1>
                    <hr>
                    <p>Наталия Григорьевна много работала и преподавала не только в России, но и в Швейцарии, Австрии,
                        Израиле, Болгарии и Турции, ведь страны разные, а проблемы у людей одинаковые</p>
                </div>
            </div>
        </div>
        <p style="text-align: justify; margin-top: 30px;">Начатый Наталией Григорьевной путь не прервался — он
            обрёл
            собственную жизнь и продолжает жить в наших сердцах. Хотя формально Школу не возродить, мы, её ученики, не
            можем
            просто отпустить то ценное, чему она нас научила.</p>
        <p style="text-align: justify;">Мы хотим и готовы делиться своими знаниями и опытом. Сегодня, в эпоху
            хронического
            стресса и цифровой перегрузки, методики Наталии Григорьевны актуальны как никогда.</p>
        <p style="text-align: justify;">Мы адаптировали авторские практики под современные реалии, сохранив их
            терапевтическую глубину и эффективность. На канале <a href="https://t.me/SchoolSelfregulation" rel="noopener" target="_blank"><strong>ВзаимоДействие </strong></a>мы проводим <strong>ежемесячные
                практические
                сессии</strong> с разбором кейсов и отвечаем на ваши вопросы.</p>
        <p style="text-align: justify;">Каждый участник становится хранителем уникальных знаний, которых не найти в
            открытых
            источниках. Это ваш шанс получить доступ к методикам, меняющим качество жизни. Также, вы можете записаться
            на <a href="https://natalie-school.ru/КОНТАКТЫ/" rel="noopener" target="_blank"> <strong>индивидуальные
                    консультации</strong></a> к наставникам.</p>
        <p style="text-align: center;"><a href="https://t.me/SchoolSelfregulation" rel="noopener" target="_blank"><button class="ui large pink basic button" style="font-family: Arsenal, sans-serif; border-radius: 20px;">TELEGRAM-КАНАЛ</button></a></p>
        <p>&nbsp;</p>
        <p style="text-align: justify;"><a class="ui labeled icon fluid teal button" href="https://natalie-school.ru" rel="noopener" style="font-family: Arsenal, sans-serif;" target="_blank"><i class="right arrow icon"></i>сайт Школы</a></p>
        <router-link :to="page.parent.to" class="ui labeled icon fluid red button" style="font-family: Arsenal, sans-serif;"><i class="left arrow icon"></i>на
            главную</router-link>
    </div>
</template>

<script setup>
import { inject, useTemplateRef, onMounted } from "vue";
import { jarallax } from "jarallax";

const { pid: id } = defineProps(["pid"]),
    page = inject("pages")[id],
    [{ url }] = page.images,
    jarallaxRef = useTemplateRef("jarallaxRef");

onMounted(() => { jarallax(jarallaxRef.value, {}) });
</script>
