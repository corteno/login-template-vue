<template>
    <div id="app">
        <!--<div id="nav">
          <router-link to="/">Home</router-link> |
          <router-link to="/about">About</router-link>
        </div>-->
        <router-view/>
    </div>
</template>

<style>
    * {
        box-sizing: border-box;
        font-family: OpensansRegular;
        color: #212121;
    }

    body, main, div, form, input, textarea, label, ul, li, header, nav, a, h1, h2, h3, button, section {
        display: flex;
    }

    body {
        height: 100%;
        margin: 0;
        background-color: #EEEEEE;
    }

    html, body{
        height: 100%;
    }

    ul {
        padding: 0;
        margin: 0;
    }

    li {
        list-style: none;
    }

    a {
        text-decoration: none;
        color: #000;
    }

    p {
        margin: 0;
    }

    #app{
        width: 100%;
        height: 100%;
    }

    .col {
        flex-direction: column;
    }

    .row {
        flex-direction: row;
    }

    input[type="submit"]{
        cursor: pointer;
        outline: none;
    }

    @font-face {
        font-family: OpensansRegular;
        src: url("./assets/fonts/OpenSans-Regular.ttf");
    }

    @font-face {
        font-family: OpensansLight;
        src: url("./assets/fonts/OpenSans-Light.ttf");
    }

    @font-face {
        font-family: OpensansBold;
        src: url("./assets/fonts/OpenSans-Bold.ttf");
    }

    @font-face {
        font-family: OpensansSemibold;
        src: url("./assets/fonts/OpenSans-SemiBold.ttf");
    }
</style>
