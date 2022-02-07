<template>
    <div>
        <p>Wise</p>
        <p class="last_p">Goat</p>
        <div class="box">
            <span>"{{message}}"</span>
            <span class="goat">- Goat</span>
        </div>
        <router-link to="/">Voltar</router-link>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data () {
        return {
            message: null
        }
    },
    methods: {
        phraseWise () {
            axios.get("https://api.adviceslip.com/advice").then((res) => {
                return this.message = res.data.slip.advice
            })
        }
    },
    mounted () {
        this.phraseWise()
    }
}
</script>

<style scoped>
div {
    padding:25px;
}
div p {
    font-size:30px;
    color:#BAA193;
    font-family: 'Roboto', sans-serif;
    font-weight: bold;
}
div .last_p {
    font-size:45px;
    color: #72005F;
    font-family: 'Roboto', sans-serif;
    font-weight: bold;
}
.box {
    width:800px;
    margin:100px auto;
    background:#ccc;
    color:#72005F;
    font-family: 'Roboto', sans-serif;
    font-weight: bold;
    padding:50px;
    font-size:25px;
    border-radius:25px;
}
.goat {
    color: rgb(111, 9, 228);
    display:inline-block;
    margin:10px 0 0 700px
}
a {
    margin:0 0 0 500px
}
</style>