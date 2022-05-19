<template>
    <div class="card-negra card-negra__orange">
        <div class="card">
            <div class="card-info">
                <div class="card-avatar">
                    <img :src="user.avatar" alt="">
                </div>
                <div class="card-info-user">
                    <div class="info-user">
                        <div class="card-name">
                            <span>Name: {{user.name}}</span>
                        </div>
                        <div class="card-subname">
                            <span>Username: {{user.username}}</span>
                        </div>
                        <div class="card-mail">
                            <span>Email: {{user.email}}</span>
                        </div>
                        <div class="card-phone">
                            <span>Phone: {{user.phone}}</span>
                        </div>
                        <div class="card-site">
                            <span>Website:  <a href="#">{{user.website}}</a></span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default{
    name: 'card-negra',
    props: [ `user` ]

}
</script>

<style lang="scss">
    

    .card-negra{
        margin: 50px 0 0 0;
        &__orange{
            background: orange;
        }
    }
    .card{
        width: 600px;

        height: 300px;
        background: #afa6af;
        &-info{
            display: flex;
        }
        &-avatar{
            width: 200px;
        }
    }
    .card-info-user{
        margin: 30px 0 0 15px;
        font-family: 'Merriweather';
        font-style: normal;
        font-weight: 900;
    }

    .card-info-user div{
        margin: 0 0 25px 0;
    }
    .card-info-user span{
        color:#ececec;
    }

    .card-site a{
        color: #ececec;
    }

    .card-site a:hover{
        text-decoration: underline;
    }
</style>