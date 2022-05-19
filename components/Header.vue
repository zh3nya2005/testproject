<template>
    <header>
      <div class="header__top__line">
        <div class="header__top__line__info">
          <div class="header__top__logo">
              <div class="logo-img">
                  <nuxt-link to="/">
                      <img src="@/static/Group.png" alt="">
                  </nuxt-link>
              </div>
              <div class="logo-title">
                  <nuxt-link to="/">
                      BunOne
                  </nuxt-link>
              </div>
          </div>
          <div class="header__link">
            <div class="header__top-link"> 
              <div v-for="c in contacts" :key="c.type" :class="`${c.type}-link` ">
                <span><img :src="c.icon" alt="">{{ c.text }}</span>
              </div>
            </div>
            <div class="header__bottom-link">
              <ul class="bottom-link">
                <li v-for="m in users" :key="m.id" >
                  <nuxt-link :to="m.avatar">{{m.username}}</nuxt-link>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </header>
</template>

<script>
export default {
    name: 'Header', 
    data(){
        return{
            users: [

            ],
            contacts: [
                {
                    text: '8 (111) 222-33-44',
                    icon: '/Vector.png',
                    type: 'phone'
                },
                {
                    text: 'Пн-Пт 10:00-18:00',
                    icon: '/Vector2.png',
                    type: 'time'
                },
                {
                    text: 'order@buhone.ru',
                    icon: '/Vector4.png',
                    type: 'mail'

                },
                {
                    text: ' Невский пр. 130',
                    icon: '/Vector5.png',
                    type: 'geo'
                },
            ],
            menubar: [
                {
                    text: 'ГЛАВНАЯ',
                    link: ''
                },
                {
                    text: 'УСЛУГИ',
                    link: ''
                },
                {
                    text: 'КЕЙСЫ',
                    link: ''
                },
                {
                    text: 'О компании',
                    link: ''
                },
                {
                    text: 'Контакты',
                    link: ''
                },
            ]
        }
    },
    async mounted(){
       let a = await this.$axios.$get('https://jsonplaceholder.ir/users')
       this.users = a;
       console.log(a)
    }
}
</script>

<style>
    
    .header__top__line {
        margin: 25px 0 0 0;
    }
    .header__top__line__info {
        display: flex;
        justify-content: space-between;
    }
    .header__top__logo {
        display: flex;
        align-items: center;
    }
    .logo-title {
        margin-left: 30px;
        width: 190px;
        font-family: 'Merriweather';
        font-style: normal;
        font-weight: 900;
        font-size: 36px;
        line-height: 50px;
    }
    .header__top-link {
        display: flex;
        margin: 0 0 30px 0;
    }

    .header__top-link span{
        margin-left: 30px;
    }

    .header__top-link img{
        margin-right: 10px;
    }
    .header__bottom-link {
        display: flex;
        justify-content: space-between;
        
    }
    .bottom-link li{
        display: inline-flex;
    }
    .bottom-link a{
        font-family: 'Lato';
        font-weight: 700;
        line-height: 17px;
        margin: 0 0 0 48px;
        color: #222222;
        letter-spacing: 0.1em;
        text-transform: uppercase;
    }

</style>