<template>
  <div class="selectBox">
      <div class="selectBox-left">
        <img src="../../assets/icon/selectUi.png" alt="">
        <div class="selectBtn">
            <div class="selectWripper">
                <span class="selectWripper-inputLeft">
                  <img class="selectWripper-imgLeft" src="../../assets/icon/sousuo.png" alt="">
                </span>
                <input type="text" name="" v-model="inputSelect" id="">
                <span class="selectWripper-inputRight">
                  <img class="selectWripper-imgRight"  src="../../assets/icon/mkf.png" alt="">
                </span>
            </div>
        </div>
      </div>
      <div class="selectBox-right">
          <img src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fgss0.baidu.com%2F7Po3dSag_xI4khGko9WTAnF6hhy%2Fzhidao%2Fpic%2Fitem%2F2e2eb9389b504fc2920bbd0de3dde71190ef6d65.jpg&refer=http%3A%2F%2Fgss0.baidu.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1642237571&t=46466614f7af24902d5cc4b6530f0e9d" alt="">
      </div>
  </div>
</template>

<script>
export default {
  name: 'appSelect',
  data () {
    return {
      message: '123',
      navList: ['主页内容1', '主页内容2'],
      inputSelect: '321'
    }
  }
}
</script>

<style scoped>
.selectBox {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  /* align-items: center; */
}
.selectBox-left {
    display: flex;
    flex-direction: column;
    align-items: center;
    flex: 7;
}
.selectBox-left>img {
    width: 300px;
    padding-top: 20px;
}
.selectBtn {
  padding-top: 30px;
}
.selectBox-right {
    flex: 3;
}
.selectBox-right img {
    width: 300px;
}
.selectWripper {
    width: 600px;
    height: 30px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 1px 1px 3px 3px rgba(235, 233, 233, 0.3);
    border-radius: 20px;
    padding: 5px 0;
}
.selectWripper input {
    outline: none;
    border: none;
    height: 100%;
    flex: 8;
}
.selectWripper-inputLeft {
    padding-left: 30px;
    flex: 1;
    display: flex;
    align-items: center;
}
.selectWripper-inputRight {
    padding-left: 30px;
    flex: 1;
    display: flex;
    align-items: center;
}
.selectWripper-imgLeft {
  width:20px !important;
  height: 20px;
}
.selectWripper-imgRight {
  width:20px !important;
  height: 20px;
}

</style>
