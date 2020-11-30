<template>
    <q-page>
        <navbar/>
        <cardLivros/>
    </q-page>
</template>

<script>
import navbar from '../components/navBar'
import cardLivros from '../components/cardLivros'
export default {
    components:{
        navbar,
        cardLivros
    }
}
</script>

<style>
    *{
        padding: 0;
        margin: 0;
    }
</style>


