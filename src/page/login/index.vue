<template>
  <div class="login-container"
       @keyup.enter.native="handleLogin">
    <div class="login-weaper  animated bounceInDown">
      <div class="login-left">
        <div class = "forImg">
          <img class="img"
               src="img/22222.png"
               alt="">
        </div>
        <p class="title">内蒙古国电信通网络科技有限公司</p>
        <p class="title2">后台管理系统</p>
      </div>
      <div class="login-border">
        <div class="login-main">
          <userLogin v-if="activeName==='user'"></userLogin>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import '@/styles/login.scss'
  import userLogin from "./userlogin";
  import {mapGetters} from "vuex";
  import {getStore, setStore} from "@/util/store";
  import {dateFormat} from "@/util/date";
  import {validatenull} from "@/util/validate";

  export default {
    name: "login",
    components: {
      userLogin
    },
    data() {
      return {
        activeName: "user"
      };
    },
    watch: {},
    created() {
    },
    mounted() {
    },
    computed: {
      ...mapGetters(["website"])
    },
    props: [],
    methods: {}
  };
</script>

