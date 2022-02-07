<template>
    <div>
        <div id="wisegoat">
            <p>Wise</p>
            <p class="last_p">Goat</p>
            <router-link to="/phrase">Pedir conselho</router-link>
        </div>
        <div id="goat">
            <img src="https://raw.githubusercontent.com/devchallenge-io/wisegoat/master/assets/bodezinho.png" alt="goat" width="400">
        </div>
    </div>
</template>

<style scoped>
div:first-child {
    width:50vw;
    height:100vh;
    color:white;
    display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background:#ccc;
}

div p:first-child {
    font-size:80px;
    color:#BAA193;
    font-family: 'Roboto', sans-serif;
    font-weight: bold;
}

div .last_p {
    font-size:120px;
    color:#72005F;
    font-family: 'Roboto', sans-serif;
    font-weight: bold;
}
div a {
    text-decoration: none;
    padding:10px 35px;
    margin-top:50px;
    background-color: #72005F;
    color:white;
    border-radius:25px;
    font-size:2rem;
    font-family: 'Roboto', sans-serif;

}

#goat {
    position:absolute;
    right:170px;
}
</style>