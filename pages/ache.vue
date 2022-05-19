<template>
    <div class="container">
        <div class="row">
            <div v-for="name in users" :key="name.id" class="col-6">
                <card-negra :user=" name " />
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'ache',
    async mounted(){
       let a = await this.$axios.$get('https://jsonplaceholder.ir/users')
       this.users = a;
       console.log(a)
    },
    data(){
        return{
            users: [
                
            ],
        }
    }
}
</script>
