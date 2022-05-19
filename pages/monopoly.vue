<template>
    <div class="container">
        <div class="row">
            <div v-for="card in cards" :key="card.id" class="col-4 mb-3">
                <kartochki  :cardMonopoly='card' />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'monopoly',
    async mounted(){
        let a = await this.$axios.$get('https://monopoly-tem4ik-default-rtdb.firebaseio.com/cards.json')
        a.forEach(el => {
            el.zalog = false
        });
        this.cards = a;
        console.log(a)
    },
    data(){
            return{
                cards: [
                ],
            }
        }
}
</script>