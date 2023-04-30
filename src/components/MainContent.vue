<template>
    <div class="login-wrap round-corner">
        <div class="content">
            <div class="background-kanban vertical-center">
                <div class="left-inside round-corner vertical-center">
                    <div>XXXXXXXXXXXX</div>
                    <img 
                    src="../assets/ErisOVO.jpg" 
                    alt="signup-img" 
                    title="ErisOvO" 
                    class="round-corner">
                    <span>已有账号？才...才不会让你登录呢</span>
                    <input 
                    type="submit" value="登录" 
                    class="init-input submit round-corner " 
                    @click="change">
                </div>
                <div class="right-inside round-corner vertical-center">
                    <div>XXXXXXXXXXXX</div>
                    <img 
                    src="../assets/ErisOVO.jpg" 
                    alt="signup-img" 
                    title="ErisOvO" 
                    class="round-corner">
                    <span>没有账号？真拿你没办法呢</span>
                    <input 
                    type="submit" value="注册"
                    class="init-input submit round-corner"
                    @click="change">
                </div>
            </div>
            <Sliding :sw="sw"/>
        </div>
    </div>
</template>

<script>
import Sliding from "./MainContent/Sliding.vue"
export default {
    components: {
        Sliding,
    },
    data() {
        return {
            sw: true,
        }
    },
    methods: {
        change() {
            this.sw = !this.sw;
        }
    },
}
</script>

<style scoped>
    .login-wrap {
        width: 600px;
        height: 350px;
        background: hsla(0, 0%, 100%, 0.25);
        box-shadow: 5px 5px 5px 0 rgba(0, 0, 0, 0.1);
    }
    .content {
        width: 100%;
        height: 100%;
        position: relative;
    }
    .content .background-kanban {
        width: 100%;
        height: 100%;
    }
    .background-kanban img {
        width: 100px;
        height: 100px;
    }
    .background-kanban img:hover {
        cursor: pointer;
    }
    .background-kanban .right-inside,
    .background-kanban .left-inside {
        flex-flow: column nowrap;
        width: 40%;
        height: 80%;
    }
    .background-kanban .submit {
        width: 60px;
        height: 30px;
        color: #FF6666;
        border: 1px solid #FF6666;
        background-color: #FFCCCC;
    }
    .background-kanban span {
        font-size: 10px;
        color: gray;
    }
    .submit:hover {
        cursor: pointer;
        background-color: #FF6666;
        color: white;
        transition: 0.5s;
    }
</style>