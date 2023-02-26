<template>
    <div class="container">
        <header class="header">
            <div class="wrapper wrapper__center">
                <img class="header__image" src="@/assets/img/banner.png" alt="banner">
                <div class="header__box">
                    <p class="header__text">Драгон Мани — онлайн казино с уникальными играми! Краш, нвути, рулетка, дабл,
                        монополия и другие! Ежедневные бонусы и праздничные события! Попробуй и получи бесплатный бонус</p>
                    <a :href="siteLink" class="button header__button">Перейти на сайт игры</a>
                </div>
            </div>
        </header>
        <section class="section section__box">
            <div class="wrapper">
                <div class="box box__strategy">
                    <div class="box__wrapper">
                        <h2 class="box__title">продумай <span class="box__title-span">стратегию</span></h2>
                        <img src="@/assets/img/coins.png" alt="coins">
                    </div>
                    <p class="box__text">Для успешной игры в казино, необходимо иметь продуманную стратегию. Хотя гемблинг -
                        это азарт, но именно правильная стратегия поможет достичь баланса между выигрышем и проигрышем.
                        Конечно, никто не может гарантировать беспроигрышную стратегию, но правильный подход поможет
                        избежать больших проигрышей и увеличить шансы на выигрыш.</p>
                    <p class="box__text">Это может начинаться с выбора подходящего казино, контроля за своими финансами и
                        выбора подходящих игр. Не забывайте, что игра в казино должна быть для вас развлечением и никогда не
                        должна становится обязанностью или способом заработка.</p>
                </div>
                <div class="box box__bonus">
                    <h2 class="box__title">бонусная<span class="box__title-span">система</span></h2>
                    <p class="box__text">"Драгон Мани" готов подарить своим лояльным игрокам массу дополнительных бонусов!
                        Привязав свой телеграм и ВК и включив двухфакторную идентификацию, вы можете получить монеты на свой
                        баланс. Даже просто после первого депозита и клика по кнопке в ЛК вы можете получить 15 монет!</p>
                    <p class="box__text">Администрация "Драгон Мани" даже платит за посещение сайта! Это делается для того,
                        чтобы заинтересовать игроков и создать активное сообщество вокруг проекта.</p>
                </div>
            </div>
        </section>
        <section>
            <h3 class="section__title">Как выбрать лучшую мини-игру на платформе?</h3>
            <p class="section__text">
                Ищете разнообразие и адреналин в игре? В Драгон Мани есть режимы, которые соответствуют вашем любимым стилям
                игры!
            </p>
            <ul class="section__list">
                <li class="section__list-item" v-for="(item, index) in list" :key="index"></li>
            </ul>
            <p class="section__text">
                Присоединяйтесь к игре на Драгон Мани и окунитесь в мир адреналина и возможностей выигрыша!
            </p>
        </section>
        <section>
            <h3 class="section__title">Как зарабатывать вместе с казино?</h3>
            <p class="section__text">
                Вы хотите зарабатывать реальные деньги, играя в автоматы? Тогда наша партнерская программа для вас! Просто
                приглашайте других участников с помощью ссылки, которую можно найти в личном кабинете. Каждый новый игрок,
                который перейдет по вашей ссылке, получит бонус в размере 50 монет, а вы получите определенный процент от
                его взносов в казино! Не упустите шанс зарабатывать деньги вместе с нами!
            </p>
            <div class="wrapper wrapper__stretch">
                <div class="box">
                    <h2 class="box__title">игровые <span class="box__title-span">новинки</span></h2>
                    <div class="games">
                        <div class="game" v-for="(game, index) of gamesList" :key="index">
                            <h5 class="game__title">{{ game.title }}</h5>
                            <ul class="game__list">
                                <li class="game__item" v-for="(option, index) of game.settings" :key="index">
                                    {{ option }}
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="box test">
                    <h2 class="box__title">Совместная разработка <span class="box__title-span">и тестирование
                            стратегий</span></h2>
                    <p class="box__text test__text">По сути, это тоже часть игры, но фокус здесь именно в использовании
                        коллективного разума и создании работающих тактик для авторских аппаратов на сайте игры.</p>
                    <p class="box__text test__text">
                        Везение — это, пожалуй, самое важное, но сформировать команду и разработать стратегию — никогда не
                        помешает. Здесь важную роль сыграет внутренний чат, который объединяет беттеров по всему миру и
                        позволяет им эффективно взаимодействовать
                    </p>
                </div>
            </div>
        </section>
        <footer>
            <p class="footer__text">
                Заходи, зарабатывай и проводи весело время с нашими играми и бонусами. Не забудь поделиться своими выигрышами с друзьями и знакомыми, которым тоже захочется поиграть и зарабатывать в Dragon Money!
            </p>
            <a :href="siteLink" class="button">Перейти на сайт игры</a>
        </footer>
    </div>
</template>

<script>

export default {
    name: 'App',
    components: {

    },
    data() {
        return {
            siteLink:'',
            list: [
                'Crash - это режим для аналитиков, где вы можете следить за графиками и предугадывать, что произойдет в следующую секунду.',
                'Dragon Dungeon - это визитная карточка казино, где азарт бьет через край. С повышенным кэфом вы можете пробить потолок выигрыша.',
                'Jackpot - это любимый режим игры для всех, где вы можете попробовать выиграть много-денег даже с одной монетки.'
            ],

            gamesList: [
                {
                    title: 'Mammoth Gold Megaways от Pragmatic Play',
                    settings: ['RTP: 96.03%', 'MAX WIN: 10 000x', ' ️MIN | MAX BET: 14₽ и 1920₽', 'VOTALlTY: HIGHT']
                },
                {
                    title: 'Rabbits Rabbits Rabbits от Endorphina',
                    settings: ['RTP: 96.05%', 'MAX WIN: 4 000x', 'MIN | MAX BET: 0.1₽ и 3600₽', 'VOTALlTY: MEDIUM | HIGHT']
                },
                {
                    title: ' Sweet Bonanza Dice от Pragmatic Play',
                    settings: ['RTP: 96.49%', 'MAX WIN: 21 100x', ' ️MIN | MAX BET: 10₽ и 6250₽', 'VOTALlTY: MEDIUM']
                },
                {
                    title: 'Fish Eye от Pragmatic Play',
                    settings: ['RTP: 96.07%', 'MAX WIN: 10 000x', ' ️MIN | MAX BET: 8₽ и 3375₽', 'VOTALlTY: HIGHT']
                },
            ]
        }
    },
}
</script>

<style lang="scss">@import '@/assets/css/style.scss'</style>
