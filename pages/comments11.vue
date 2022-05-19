<template>
    <div class="container">
        <div class="background__png">
            <div class="main__png">
                <div class="png">
                    <img src="@/static/mountains-snow-grass-water-plants-sky-1011450.jpg" alt="">
                </div>
            </div>
        </div>
        <div class="row">
            <div v-for="comm in comms" :key="comm.id" class="col-3 mb-3">
                <Comments :coms='comm' />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Comments11',
    async mounted(){
        let a = await this.$axios.$get('https://gorest.co.in/public/v2/comments')
        this.comms = a;
        console.log(a)
    },
    data(){
            return{
                comms: [
                ],
            }
        }
}
</script>
