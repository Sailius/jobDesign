<script lang="ts">
	import Header from './Header.svelte';
    import Bubble from './Bubble.svelte';
    import Block from './Block.svelte';
    import Splash from './Splash.svelte';
	import Advantage from './Advantage.svelte';
</script>

<div class="root">
    <Header />
    <div class="content">
        <div>
            <Block procentage={15} />
            <Block procentage={45} >
                <h1>
                    Стикеры А4 в общественном транспорте Балашихи — 
                    это ваш шанс поймать взгляд клиента, пока он
                    заскучавши едет сквозь вечерние пробки.
                </h1>
            </Block>
            <Block procentage={35}>
                <img
                    id="stickerFox"
                    src="/images/CloudFox.png"
                    alt="Внутрисалонная реклама на стикерах А4"
                />
            </Block>
            <Bubble order="first" />
            <Bubble order="second" />
        </div>
        <div>
            <Block procentage={5} />
            <Block procentage={45}>
                <Splash procentage={90} type={1}>
                    <div class="splash_content first">
                        <img
                            id="realPicture"
                            src="/images/irlPicture.jpg"
                            alt="Рисунок стикера А4 в автобусе"
                        />
                        <Advantage
                            img_name={"clock"}
                            title={"Срок жизни стикеров - от трёх до шести месяцев."}
                        />
                        <Advantage
                            img_name={"money"}
                            title={"Средняя цена за тысячу контактов - всего от 5 руб."}
                        />
                    </div>
                </Splash>
            </Block>
            <Block procentage={50}>
                <div class="little_column">
                    <Splash procentage={20} type={2}>
                        <div class="splash_content">
                            <img
                                id="stickerDrawing"
                                src="/images/StickersA4.jpg"
                                alt="Рисунок стикера А4 в автобусе"
                            />
                            <div class="splash_text">
                                <h2>Формат А4</h2>
                                <p>
                                    Совсем не перегружает пространство,
                                    при этом хорошо читаем.
                                </p>
                            </div>
                        </div>
                    </Splash>
                    <Advantage img_name={"eye"} title={"Цепляет взгляд"}>
                        Ловит пассажиров в пробках Щёлковского шоссе — 20+ минут контакта.
                    </Advantage>
                    <Advantage img_name={"aim"} title={"Точный охват"}>
                        Прицельно бьёт по районам через нужные маршруты:
                        Железнодорожный, Салтыковка, Гагарина.
                    </Advantage>
                    <Advantage img_name={"box"} title={"Доставка до дверей"}>
                        Гиперлокально для бизнеса у остановок: "Вы выходите? Мы рядом!"
                    </Advantage>
                </div>
            </Block>
        </div>
        <div>
            <Block procentage={5} />
            <Block procentage={20}>
                <h3>С нами работали</h3>
                <div class="famous_clients">
                    <div>
                        <img src="/images/logo_5.png" alt="company1">
                        <img src="/images/logo_rostech.jpg" alt="company2">
                        <img src="/images/logo_5.png" alt="company3">
                        <img src="/images/logo_rostech.jpg" alt="company4">
                        <img src="/images/logo_5.png" alt="company5">
                        <img src="/images/logo_rostech.jpg" alt="company6">
                    </div>
                </div>
            </Block>
            <Block procentage={30}>
                <img
                    id="busFox"
                    src="/images/BusFox01.png"
                    alt="Лисёнок, играющий с автобусом"
                />
            </Block>
            <Block procentage={40}>
                <form action="/123" method="post">
                    <h2>Запрос коммерческого предложения</h2>
                    <input type="text" name="" id="" placeholder="Компания / Имя"/>
                    <input type="email" name="" id="" placeholder="E-mail"/>
                    <input type="text" name="" id="" placeholder="Телефон"/>
                    <div class="button">Отправить заявку</div>
                    <p>
                        *Нажимая кнопку, Вы даёте согласие
                        на <span>обработку персональных данных</span>
                    </p>
                </form>
            </Block>
            <Block procentage={5} />
        </div>
        <div>
            <Block procentage={100}>
                <h2 class="central_heading">Отзывы</h2>
            </Block>
        </div>
        <div>
            <Block procentage={5} />
            <Block procentage={90}>
                <div class="reviews">
                    <div class="left_arrow">{'<'}</div>
                    <div class="right_arrow">{'>'}</div>
                    <p class="reviewer_name">Автошкола</p>
                    <div class="review_content">
                        <p>
                            {`Ребята, вы прекрасная команда! Всё делаете оперативно,
                            всегда на связи, добываете рекламные места чётко под запрос))
                            С вами приятно иметь дело, успехов вам и процветания!`}
                        </p>
                        <p>
                            {`Егор, Вам отдельное спасибо за сотрудничество!`}
                        </p>
                    </div>
                </div>
            </Block>
            <Block procentage={5} />
        </div>
    </div>
</div>

<style>
    

    .root {
        display: flex;
        justify-content: center;
        font-family: 'Montserrat';
    }

    .content {
        width: 100%;
        background: linear-gradient(135deg, #cdffcf 7%, #eee 55%, #ffebcd 120%);
    }
    .content > div {
        padding: 1%;
        overflow: hidden;
        position: relative;
        display: flex;
        z-index: 400;
    }
    
    .content > div:nth-of-type(1) {
        height: 500px;
        padding-top: 90px;
    }

    .content > div:nth-of-type(2) {
        min-height: 575px;
    }

    .content > div:nth-of-type(3) {
        height: 500px;
    }

    h1 {
        width: 90%;
        font-size: 32px;
        font-weight: 600;
    }

    img#stickerFox {
        height: 320px;
        width: 320px;
    }

    img#realPicture {
        width: 100%;
        border-radius: 10px;
    }

    .little_column {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 60%;
        height: 90%;
        gap: 45px;
    }

    .splash_content {
        display: flex;
        height: 100%;
        width: 100%;
        align-items: center;
        justify-content: center;
        gap: 15px;
    }

    .splash_content.first {
        align-items: flex-start;
        flex-direction: column;
    }

    img#stickerDrawing {
        height: 85px;
        border-radius: 5px;
    }

    .splash_text {
        display: flex;
        flex-direction: column;
        height: 100%;
        width: 100%;
        align-items: flex-start;
        justify-content: center;
        gap: 7px;
    }

    .splash_text > p {
        font-size: 18px;
    }

    h2 {
        font-weight: 600;
    }

    h3 {
        width: 200px;
        text-align: center;
        text-transform: uppercase;
        font-weight: 600;
        font-size: 26px;
    }

    .famous_clients {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
    }

    .famous_clients > div {
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        width: 100%;
        height: 100%;
    }

    .famous_clients > div > img {
        cursor: pointer;
        width: 60px;
        height: 60px;
        border-radius: 50%;
        position: absolute;
    }

    .famous_clients > div > img:nth-of-type(1) { transform: translate(0, -150px); }
    .famous_clients > div > img:nth-of-type(2) { transform: translate(0, 150px); }
    .famous_clients > div > img:nth-of-type(3) { transform: translate(130px, 75px); }
    .famous_clients > div > img:nth-of-type(4) { transform: translate(130px, -75px); }
    .famous_clients > div > img:nth-of-type(5) { transform: translate(-130px, 75px); }
    .famous_clients > div > img:nth-of-type(6) { transform: translate(-130px, -75px); }

    img#busFox {
        height: 350px;
    }

    form {
        position: relative;
        background-color: #eee;
        width: 90%;
        height: 90%;
        display: flex;
        flex-direction: column;
        gap: 30px;
        justify-content: space-evenly;
        align-items: center;
        border: 2px solid #ffe;
        padding: 15px;
        padding-bottom: 50px;
        border-radius: 10px;
        background: linear-gradient(135deg, #eee, #feebce);
    }

    form > h2 {
        font-size: 28px;
        font-weight: 500;
    }

    form > p {
        position: absolute;
        bottom: 20px;
        color: #777;
    }

    form > p > span {
        cursor: pointer;
        border-bottom-width: 1px;
        border-bottom-style: dashed;
    }

    form > p > span:hover {
        color: #010101;
    }

    input {
        width: 300px;
        height: 40px;
        border: none;
        border-radius: 10px;
        padding: 5px 10px;
        font-size: 20px;
    }

    input:focus {
        outline: none;
        border: none;
        box-shadow: inset 0 0 1px 2px #01010140;
    }

    .button {
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 300px;
        height: 50px;
        padding: 5px;
        color: #fff;
        border-radius: 10px;
        font-size: 22px;
        font-weight: 550;
        background-color: #01010140;
        transition: ease 0.25s;
    }

    .button:hover {
        background-color: #01010180;
    }
    
    .central_heading {
        font-size: 40px;
    }

    .reviews {
        display: grid;
        grid-template-rows: 45px 30px 10px 240px 45px;
        grid-template-columns: 45px 30px 60px auto 30px 45px;
        width: 70%;
        height: 370px;
        background-color: #eee;
        /* background: linear-gradient(135deg, #eee, #feebce 120%); */
        border: 2px solid #ffe;
        border-radius: 10px;
    }

    .reviews > * {
        display: flex;
        justify-content: center;
    }

    .left_arrow, .right_arrow {
        user-select: none;
        cursor: pointer;
        max-height: 366px;
        /* background-color: #01010120; */
        background-color: #01010120;
        opacity: 0;
        align-items: center;
        font-size: 32px;
        color: #eee;
        transition: ease 0.5s;
    }

    .reviews:hover > .left_arrow, .reviews:hover > .right_arrow {
        opacity: 1;
    }

    .left_arrow {
        grid-area: 1 / 1 / span 5 / span 1;
        border-radius: 10px 0 0 10px;
    }

    .right_arrow {
        grid-area: 1 / 6 / span 5 / span 6;
        border-radius: 0 10px 10px 0;
    }

    .reviewer_name {
        cursor: pointer;
        grid-area: 2 / 4 / 3 / 5;
        width: fit-content;
        font-size: 28px;
        font-weight: 600;
        text-decoration: underline;
    }

    .review_content {
        grid-area: 4 / 3 / 5 / 5;
        flex-direction: column;
        align-items: flex-start;
        gap: 15px;
        font-size: 24px;
    }
</style>