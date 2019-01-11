<script>
  import {get, showSuccess} from './utils/index'
  import qcloud from 'wafer2-client-sdk'
  import config from './config'
  export default {
    data () {
      return {}
    },
    async created () {
      let user = wx.getStorageSync('userinfo')
      if (!user) {
        qcloud.setLoginUrl(config.loginUrl)
        wx.login({
          success: function (userInfo) {
            console.log('登录成功', userInfo)
          },
          fail: function (err) {
            console.log('登录失败', err)
          }
        })
      }
      /*let res = await get('demo')
      console.log(res)*/
    }
  }
</script>

<style scoped>

</style>
