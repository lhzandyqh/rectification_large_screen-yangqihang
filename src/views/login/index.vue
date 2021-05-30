<template>
  <div class="login-container">
    <div>
      <div style="text-align: center;width: 500px;height: 500px;position: absolute;left: 50%;top: 50%;transform: translate(-50%, -50%)">
        <img :src="loadingImg" style="width: 100%">
      </div>
    </div>
    <!--    <el-form ref="loginForm" :model="loginForm" :rules="loginRules" class="login-form" auto-complete="on" label-position="left">-->
    <!--      <div class="title-container">-->
    <!--        <h3 class="title">-->
    <!--          {{ $t('login.title') }}-->
    <!--        </h3>-->
    <!--        <lang-select class="set-language" />-->
    <!--      </div>-->

    <!--      <el-form-item prop="username">-->
    <!--        <span class="svg-container">-->
    <!--          <svg-icon icon-class="user" />-->
    <!--        </span>-->
    <!--        <el-input-->
    <!--          ref="username"-->
    <!--          v-model="loginForm.username"-->
    <!--          :placeholder="$t('login.username')"-->
    <!--          name="username"-->
    <!--          type="text"-->
    <!--          auto-complete="on"-->
    <!--        />-->
    <!--      </el-form-item>-->

    <!--      <el-form-item prop="password">-->
    <!--        <span class="svg-container">-->
    <!--          <svg-icon icon-class="password" />-->
    <!--        </span>-->
    <!--        <el-input-->
    <!--          ref="password"-->
    <!--          v-model="loginForm.password"-->
    <!--          :type="passwordType"-->
    <!--          :placeholder="$t('login.password')"-->
    <!--          name="password"-->
    <!--          auto-complete="on"-->
    <!--          @keyup.enter.native="handleLogin"-->
    <!--        />-->
    <!--        <span class="show-pwd" @click="showPwd">-->
    <!--          <svg-icon :icon-class="passwordType === 'password' ? 'eye' : 'eye-open'" />-->
    <!--        </span>-->
    <!--      </el-form-item>-->

    <!--      <el-button :loading="loading" type="primary" style="width:100%;margin-bottom:30px;" @click.native.prevent="handleLogin">-->
    <!--        {{ $t('login.logIn') }}-->
    <!--      </el-button>-->

    <!--      <div style="position:relative">-->
    <!--        <div class="tips">-->
    <!--          <span>{{ $t('login.username') }} : admin</span>-->
    <!--          <span>{{ $t('login.password') }} : {{ $t('login.any') }}</span>-->
    <!--        </div>-->
    <!--        <div class="tips">-->
    <!--          <span style="margin-right:18px;">-->
    <!--            {{ $t('login.username') }} : editor-->
    <!--          </span>-->
    <!--          <span>{{ $t('login.password') }} : {{ $t('login.any') }}</span>-->
    <!--        </div>-->

    <!--        <el-button class="thirdparty-button" type="primary" @click="showDialog=true">-->
    <!--          {{ $t('login.thirdparty') }}-->
    <!--        </el-button>-->
    <!--      </div>-->
    <!--    </el-form>-->

    <!--    <el-dialog :title="$t('login.thirdparty')" :visible.sync="showDialog">-->
    <!--      {{ $t('login.thirdpartyTips') }}-->
    <!--      <br>-->
    <!--      <br>-->
    <!--      <br>-->
    <!--      <social-sign />-->
    <!--    </el-dialog>-->
  </div>
</template>

<script>
import { validUsername } from '@/utils/validate'
// import LangSelect from '@/components/LangSelect'
// import SocialSign from './socialsignin'

export default {
  name: 'Login',
  // components: { LangSelect, SocialSign },
  data() {
    const validateUsername = (rule, value, callback) => {
      if (!validUsername(value)) {
        callback(new Error('Please enter the correct user name'))
      } else {
        callback()
      }
    }
    const validatePassword = (rule, value, callback) => {
      if (value.length < 6) {
        callback(new Error('The password can not be less than 6 digits'))
      } else {
        callback()
      }
    }
    return {
      loadingImg: 'http://zhongkeruitong.top/zgbigscreen-show/loading.gif',
      loginForm: {
        username: 'admin',
        password: '111111'
      },
      loginRules: {
        username: [{ required: true, trigger: 'blur', validator: validateUsername }],
        password: [{ required: true, trigger: 'blur', validator: validatePassword }]
      },
      passwordType: 'password',
      loading: false,
      showDialog: false,
      redirect: undefined
    }
  },
  watch: {
    $route: {
      handler: function(route) {
        this.redirect = route.query && route.query.redirect
      },
      immediate: true
    }
  },
  created() {
    // window.addEventListener('hashchange', this.afterQRScan)
  },
  mounted() {
    if (this.loginForm.username === '') {
      this.$refs.username.focus()
    } else if (this.loginForm.password === '') {
      this.$refs.password.focus()
    }
    setTimeout(() => {
      this.handleLogin()
    }, 1500)
  },
  destroyed() {
    // window.removeEventListener('hashchange', this.afterQRScan)
  },
  methods: {
    showPwd() {
      if (this.passwordType === 'password') {
        this.passwordType = ''
      } else {
        this.passwordType = 'password'
      }
      this.$nextTick(() => {
        this.$refs.password.focus()
      })
    },
    // handleLogin() {
    //   this.$refs.loginForm.validate(valid => {
    //     if (valid) {
    //       this.loading = true
    //       this.$store.dispatch('LoginByUsername', this.loginForm).then(() => {
    //         this.loading = false
    //         this.$router.push({ path: this.redirect || '/' })
    //       }).catch(() => {
    //         this.loading = false
    //       })
    //     } else {
    //       console.log('error submit!!')
    //       return false
    //     }
    //   })
    // },
    handleLogin() {
      this.$store.dispatch('LoginByUsername', this.loginForm).then(() => {
        this.loading = false
        this.$router.push({ path: this.redirect || '/' })
      }).catch(() => {
        this.loading = false
      })
    },
    afterQRScan() {
      // const hash = window.location.hash.slice(1)
      // const hashObj = getQueryObject(hash)
      // const originUrl = window.location.origin
      // history.replaceState({}, '', originUrl)
      // const codeMap = {
      //   wechat: 'code',
      //   tencent: 'code'
      // }
      // const codeName = hashObj[codeMap[this.auth_type]]
      // if (!codeName) {
      //   alert('第三方登录失败')
      // } else {
      //   this.$store.dispatch('LoginByThirdparty', codeName).then(() => {
      //     this.$router.push({ path: '/' })
      //   })
      // }
    }
  }
}
</script>

<style rel="stylesheet/scss" lang="scss">

</style>
