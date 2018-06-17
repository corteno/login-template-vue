<template>
    <form action="" class="login-form col">
        <h1 class="form-title">{{title}}</h1>
        <label for="email" class="form-label row" v-if="title === 'Sign Up'">
            <img src="../assets/img/mail.svg" alt="" class="form-input-image">
            <input id="email" type="email" class="form-text-input" placeholder="E-mail">
        </label>

        <label for="username" class="form-label row">
            <img src="../assets/img/user.svg" alt="" class="form-input-image">
            <input id="username" type="text" class="form-text-input" placeholder="Username">
        </label>
        <label for="password" class="form-label row">
            <img src="../assets/img/lock.svg" alt="" class="form-input-image">
            <input id="password" type="password" class="form-text-input" placeholder="Password">
        </label>
        <input type="submit" class="form-submit" v-bind:value="title">
        <p class="form-switch" v-on:click="e => switchMode(e)">{{switchTo}}</p>
    </form>
</template>

<script>
    export default {
        name: "LoginForm",
        props: {
            title: String,
            switchTo: String,
            switchMode: Function
        }
    }
</script>

<style>
    .login-form {
        max-width: 350px;
        width: 100%;
        height: auto;

        background: #fff;
        border-radius: 6px;
        box-shadow: 0 2px 2px rgba(0, 0, 0, 0.2);
        /*padding: 20px 0;*/
        padding-bottom: 20px;
        overflow: hidden;
    }

    .form-title {
        text-align: center;
        justify-content: center;
        margin: 0 0 40px;
        padding: 20px 0;
        color: #fafafa;
        letter-spacing: 1px;
        font-family: OpensansRegular, sans-serif;
        text-transform: uppercase;
        background: linear-gradient(to right, #DA4453, #89216B);
    }

    .form-label {
        position: relative;
        padding: 0 20px;
        margin-bottom: 20px;
    }
    .form-input-image {
        border-top-left-radius: 4px;
        border-bottom-left-radius: 4px;
        border: 1px solid #EC407A;
        padding: 0 5px;
    }

    .form-text-input {
        width: 100%;
        border-bottom-right-radius: 4px;
        border-top-right-radius: 4px;
        padding: 8px 10px;
        outline: none;
        border: 1px solid #EC407A;
        border-left: 0;
    }

    .form-submit {
        margin: 20px 20px 0;
        justify-content: center;
        padding: 15px 35px;
        border-radius: 4px;
        color: #E91E63;
        font-family: OpensansSemibold, sans-serif;
        font-size: 16px;
        text-transform: uppercase;
        background: transparent;
        border: 2px solid #E91E63;
        transition: 0.2s all;
    }

    .form-submit:hover {
        background: #E91E63;
        color: #fafafa;
    }

    .form-switch{
        text-align: center;
        justify-content: center;
        color: #E91E63;
        margin-top: 10px;
        font-family: OpensansSemibold, sans-serif;
        cursor: pointer;
        align-self: center;
        user-select: none;
    }

    .form-switch:hover{
        text-decoration: underline;
    }

    @media only screen and (max-width: 600px) and (max-height: 800px) {
        .login-wrapper {
            background: none;
        }

        .login-form {
            max-width: 600px;
            width: 100%;
            height: auto;
            min-height: 100%;
            overflow-y: scroll;
            border-radius: 0;
        }
    }


</style>