<template>
  <div class="headerBox">
    <div class="headerLogo">
      <div class="welComeLogo">
        <img src="../../assets/icon/bookLogo.png" alt="图片丢了">
        <span>welCome To JunUI</span>
      </div>
      <div class="headerName">
          <img src="../../assets/icon/logoOne.png" alt="图片丢了">
          <img src="../../assets/icon/logoThree.png" alt="图片丢了">
      </div>
    </div>
    <nav class="headerNav" >
      <div class="navContent" v-for="(item,index) in navList" :key="index">{{item}}</div>
    </nav>
    <div class="headerUser">
      <img src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fwww.xplian.net%2FtuxpJDEwLmFsaWNkbi5jb20vaTIvMzAwMDE0NTg0NS9PMUNOMDE5UFhsdUMxdDMzVXVybUNFb18hITMwMDAxNDU4NDUkOQ.jpg&refer=http%3A%2F%2Fwww.xplian.net&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1642234173&t=52310ccf9ef2ec62df6f968dc9684ec8" alt="图片丢了">
      <img src="../../assets/icon/down.png" alt="图片丢了">
    </div>
  </div>
</template>

<script>
export default {
  name: 'appHeader',
  data () {
    return {
      message: '123',
      navList: ['主页内容1', '主页内容2']
    }
  }
}
</script>

<style scoped>
.headerBox {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 20px 150px;
}
.headerLogo {
  font-weight: bold;
  text-align: center;
  display: flex;
  align-items: center;
  flex: 7;
}
.welComeLogo {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.headerLogo img {
  width: 60px;
}
.headerName {
  padding-left: 20px;
  display: flex;
  align-items: center;
}
.headerName img:first-child {
  width: 30px;
  height: 30px;
}
.headerName img:last-child {
  width: 35px;
  height: 35px;
}
.headerName span {
  padding-left: 5px;
  font-weight: bold;
}
.headerNav {
  display: flex;
  align-items: center;
  flex: 20;
}
.navContent {
  padding: 0 10px;
}
.headerUser {
  display: flex;
  align-items: center;
  flex: 5;
}
.headerUser img:first-child {
  widows: 40px;
  height: 40px;
  border-radius: 50%;
}
.headerUser img:last-child {
  widows: 20px;
  height: 20px;
}
</style>
