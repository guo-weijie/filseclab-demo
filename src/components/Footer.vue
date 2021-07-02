<template>
  <div class="footer">
    <div class="footerBox">
      <div>
        <span>© Filseclab Corporation 京ICP备09054277号</span>
        <span class="pointer ml">友情链接</span>
        |
        <span class="pointer">隐私条款</span>
      </div>
      <div>
        <span class="pointer">首页</span>
        |
        <span class="pointer">产品</span>
        |
        <span class="pointer">联系我们</span>
        <a class="ml" href="http://facebook.com/filseclab"><img src="http://filseclab.com/images/logo_facebook.png" alt="" /></a>
        <a class="ml" href="http://twitter.com/filseclab"><img src="http://filseclab.com/images/logo_twitter.png" alt="" /></a>
        <a class="ml" href="http://www.linkedin.com/in/filseclab"><img src="http://filseclab.com/images/logo_linkedin.png" alt="" /></a>
        <a class="ml" href="mailto:kefu@filseclab.com"><img src="http://filseclab.com/images/logo_email.png" alt="" /></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer {
  height: 0.48rem;
  background-color: #696969;
  color: #fff;
  font-size: .12rem;
  .footerBox {
    width: 12rem;
    height: .48rem;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
.pointer{
    cursor: pointer;
}
.ml{
    margin-left: .5em;
    img{
        vertical-align: middle;
        transform: translateY(-2px);
    }
}
</style>