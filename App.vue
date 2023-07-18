<script>
export default {
  onLaunch: function () {
    console.log('App Launch')
  },
  onShow: function () {
    console.log('App Show')
    const howxm = requirePlugin('howxm-plugin') //引入浩客sdk
    howxm.debug(true) //开启debug模式
    howxm.init( //进行初始化
        '6c00f0b6-7f7e-47e7-b2be-e0324a6a15dc',
        {},
        function (data) {
          console.log("init success:", data)
        },
        function (err) {
          // 失败回调
        }
    )
  },
  onHide: function () {
    console.log('App Hide')
  }
}
</script>

<style>
/*每个页面公共css */
</style>
