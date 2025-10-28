<template>
    <div ref="jarallaxRef" class="ui basic vertical fitted segment jarallax mceNonEditable  min-h-[60vh]"
        :style="`background-image:url(${url})`">
        <div class="ui active light dimmer">
            <div class="content"><a class="ui header hvr-icon-wobble-vertical massive inverted icon"
                    style="font-family: Arsenal, sans-serif;"><i class="hvr-icon !h-28 icon mx-auto"
                        :class="page.i"></i><span class="ui">{{ page.title }}<span class="sub header">{{
                            page.description
                            }}</span></span></a></div>
        </div>
    </div>
    <p>&nbsp;</p>
    <div class="ui container">
        <div class="ui dividing header" style="font-family: Arsenal, sans-serif;">НАТАЛИЯ НОСАЧЕВА:
            <div class="sub header">многие события в моей жизни начинались со слова "вдруг"</div>
        </div>
        <p style="text-align: justify;">В феврале 2009 года звонок из Государственной Думы был для меня неожиданным.
            Оказывается, рассказ о моей деятельности с фотографией включили в книгу "Лучшие люди России". Но это было
            ещё не
            всё. Меня наградили орденом I степени "За профессиональную честь, достоинство и почётную профессиональную
            репутацию". Это не первая моя награда. Но каждая по особому дорога. А когда разглядываю этот орден, в душе
            вспыхивает гордость. Нет, не зря отдаю все свои знания, все умения для того, чтобы исцелять людей. И на
            Земле
            живу не напрасно!</p>
        <p>&nbsp;</p>
        <div class="ui horizontal stackable segments">
            <div class="ui segment">
                <p><iframe style="width: 100%;" src="https://player.vimeo.com/video/262984670?h=9d67bd1461"
                        frameborder="0" allowfullscreen="true"></iframe></p>
                <p style="text-align: center;">Наталия Носачева о Школе саморегуляции</p>
            </div>
            <div class="ui segment">
                <p><iframe style="width: 100%;" src="https://player.vimeo.com/video/1091475094" frameborder="0"
                        allowfullscreen="true"></iframe></p>
                <p style="text-align: center;">Большое интервью Наталии Григорьевны</p>
            </div>
            <div class="ui segment">
                <p><iframe style="width: 100%;" src="https://player.vimeo.com/video/700012228?h=1c996d0a48"
                        frameborder="0" allowfullscreen="true" class="ma-auto"></iframe></p>
                <p style="text-align: center;">Награждение в Госдуме,интервью с<br>Наталией Григорьевной с 6 минут 50
                    секунд
                </p>
            </div>
            <div class="ui segment">
                <p><iframe style="width: 100%;" src="https://player.vimeo.com/video/252848734?h=bca1146c42"
                        frameborder="0" allowfullscreen="true" class="ma-auto"></iframe></p>
                <p style="text-align: center;">Поиск машины Леры Кудрявцевой</p>
            </div>
            <div class="ui center aligned segment">
                <p><iframe src="https://rutube.ru/play/embed/ee1bf545cf0c4ef4aa1483fb18db8d8b" frameborder="0"
                        allowfullscreen="true" class="ma-auto"></iframe></p>
                <p style="text-align: center;">Запись вебинара Наталии Носачевой</p>
            </div>
            <div class="ui center aligned segment">
                <p><iframe src="https://rutube.ru/play/embed/b93b03481aee06a4332d8b94390d47c2" frameborder="0"
                        allowfullscreen="true" class="ma-auto"></iframe></p>
                <p style="text-align: center;">Курсы саморегуляции Наталии Носачевой</p>
            </div>
            <div class="ui center aligned segment">
                <p><iframe src="https://rutube.ru/play/embed/755b4bbdb1fd464af4ade5caf15dc0ad" frameborder="0"
                        allowfullscreen="true" class="ma-auto"></iframe></p>
                <p style="text-align: center;">Наталия Носачева о программе онлайн Школы</p>
            </div>
            <div class="ui center aligned segment">
                <p><iframe src="https://rutube.ru/play/embed/bc6140bb01f42d3e8bfe9c2d84ba92ec" frameborder="0"
                        allowfullscreen="true" class="ma-auto"></iframe></p>
                <p style="text-align: center;">Наталия Носачева отвечает на вопросы</p>
            </div>
        </div>
        <p>&nbsp;</p>
        <router-link :to="page.parent.to" class="ui labeled icon fluid red button"
            style="font-family: Arsenal, sans-serif;"><i class="left arrow icon"></i>на
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