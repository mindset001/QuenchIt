<template >
    <div class="own">
        <div class="container">
        <h4 class="header">
            {{ cardsSection.title }}
        </h4>
        <p class="snippet" >
            {{ cardsSection.snippet }}
        </p>
        <div class="cards-container">
             <LargeCard 
                v-for="card in cardsSection.cards"
                :key="card.image"
                :card="card"
            />
        </div>
    </div>
    </div>
</template>

<script>
    export default {
        props: ['cardsSection']
    }
</script>

<style scoped>
.own{
    margin-top: 10rem;
}
.container {
    margin-top: 2rem;
}
    .header {
        font-weight: 700;
        font-size: 1.5rem;
    }
    .snippet {
        color: grey;
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }
</style>