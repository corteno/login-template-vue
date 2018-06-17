<template>
    <div class="login-wrapper">
        <LoginForm v-bind:title="activeMode" v-bind:switchMode="switchMode" v-bind:switchTo="inactiveMode" />
    </div>
</template>

<script>
    import LoginForm from '@/components/LoginForm.vue';

    let switchMode = function(e) {
        e.preventDefault();
        let temp = this.activeMode;
        this.activeMode = this.inactiveMode;
        this.inactiveMode = temp;
        //console.log(this.activeMode);
    };

    export default {
        name: "Login",
        components: {
            LoginForm
        },
        data: () => {
            return {
                isLogin: true,
                activeMode: 'Sign In',
                inactiveMode: 'Sign Up'
            }
        },
        methods: {
            switchMode
        }
    }


</script>

<style scoped>
    .login-wrapper {
        width: 100%;
        min-height: 100%;
        justify-content: center;
        align-items: center;
        /*background: url("../assets/img/abstract-art-artistic-796607.jpg") center center;*/
        background: url("../assets/img/abstract-art-artistic-796607.jpg");
        background-size: cover;
    }

    @media only screen and (max-width: 600px) and (max-height: 800px) {
        .login-wrapper {
            background: none;
        }
    }
</style>