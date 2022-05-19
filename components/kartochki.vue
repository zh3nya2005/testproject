<template>
    <div class="container">
        <div class="bg__card">
            <div class="wrapper__card">
                <div class="content__card">
                    <div class="header__card" :style="`background: ${cardMonopoly.group}`"> 
                        <div class="heading__title">
                            <span>Карточка собственника</span>
                        </div>
                        <div class="heading__subtitle">
                            <span v-if="cardMonopoly.zalog">Заложен</span>
                            <span>{{cardMonopoly.name}}</span>
                        </div>
                    </div>
                    <div class="nav_card">
                        <div class="nav__title">
                            <span>Рента с участка {{cardMonopoly.pay}}</span>
                        </div>
                        <div class="nav__info">
                            <div class="info__house-link w-100">
                                <div v-for="pay in cardMonopoly.pays" :key="pay.name" class="d-flex justify-content-between">
                                    <span class="d-flex">{{pay.name}}</span> <span class="d-flex">{{pay.price}}</span>
                                </div>
                            </div>
                        </div>
                        <div class="nav__other__info ">
                            <ul class="info__other__info-link">
                                <li>Залог участка {{cardMonopoly.sell}}</li>
                                <li>Цена домов {{cardMonopoly.house}}</li>
                                <li>Цена отелей {{cardMonopoly.house}}</li>
                                <li>плюс 4 дома</li>
                            </ul>
                        </div>
                    </div>
                    <div class="footer__card">
                        <div class="footer__info">
                            <span>Если игрок владеет всеми участками одного цвета, рента с незастроенных участков этого цвета удваивается</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'kartochki',
    props: [ `cardMonopoly` ]
}
</script>

<style>
    .bg__card {
        letter-spacing: 1px;
        border: 1px solid gray;
        margin-top: 30px;
        background: rgb(226, 225, 225);
        width: 300px;
        border-radius: 4px;
    }
    .wrapper__card {
        display: flex;
        flex-direction: column;
        min-height: 100%;
    }
    .content__card{
        font-family: Arial, Helvetica, sans-serif;
        text-align: center;
        flex: 1 0 auto;
    }
    .header__card {
        font-weight: bold;
        text-align: center;
        margin: 11px;
        padding: 5px;
        text-transform: uppercase;
        border: 1px solid #000;
    }
    .heading__title {
        padding-top: 5px;
        padding-bottom: 15px;
    }
    .heading__subtitle {
        padding-bottom: 13px;
        font-weight: 900;
        font-size: 18px;
    }
    .nav_card {
        flex: 1 1 auto;
        text-align: center;
    }
    .nav__title {
        font-weight: bold;
        font-size: 17px;
        margin: 0 0 15px 0;
    }
    .nav__info {
        display: flex;
        justify-content: space-between;
        margin: 0 7px;
    }
    .nav__info li{
        margin: 0 0 3px 0;
    }
    .info__house-link li{
        display: flex;
        justify-content: space-between;
    }
    .info__other__info-link li{
        margin: 0 0 5px 0;
    }
    .info__other__info-link li:nth-child(1){
        font-weight: 700;
        
    }
    .footer__card {
        flex: 0 0 auto;
    }
    .footer__info {
        padding: 0 40px;
        font-size: 10px;
        margin: 0 0 15px 0;
        font-size: 13px;
    }
</style>