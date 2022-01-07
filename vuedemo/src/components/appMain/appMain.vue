<template>
  <div class="mainBox">
      <div class="allNotes">
          <div class="notesContent" v-for="(item,index) in list" :key="index" :style="{height: topList[index]+'px',left: leftSet(index)+'px',top: topSet(index)+'px'}" style="background: url('https://picsum.photos/200/250')">
            <div class="notesLine">{{item}}</div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'appSelect',
  data () {
    return {
      msg: '123',
      list: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15],
      rangeHeight: 0,
      topList: []
    }
  },
  mounted () {
    this.list.filter(() => {
      this.topList.push(this.difBox())
    })
    console.log(this.topList)
  },
  methods: {
    difBox () {
      const minHeight = 150
      const maxHeight = 250
      // 随机高度
      const rangeHeight = Math.floor(Math.random() * (maxHeight - minHeight + 1) + minHeight)
      // this.topList.splice(-1, 0, rangeHeight)
      // console.log(this.topList)
      return rangeHeight
    },
    leftSet (e) {
      const leftPx = e % 6 * 205
      return leftPx
    },
    topSet (indexa) {
      if (indexa < 6) {
        return 0
      } else {
        const topJg = indexa % 6
        let topPx = 0
        for (let i = 0; i < indexa; i++) {
          if (i % 6 === topJg) {
            topPx += this.topList[i]
          }
        }
        topPx += Math.ceil(indexa / 6 - 1) * 5
        console.log(topPx)
        return topPx
      }
    }
  }
}
</script>

<style scoped>
.mainBox {
    margin-top: 50px;
}
.allNotes {
    /* display: flex;
    flex-direction: column;
    gap: 5px;
    flex-wrap: wrap; */
    position: relative;
}
.notesContent {
    width: 200px;
    position: absolute;
    font-size: 30px;
    color: beige;
    overflow: hidden;
    box-sizing: border-box;
    cursor:pointer;
    /* 灰度模式 grayscale */
    /* filter: grayscale(100%); */
}
.notesContent::after {
  content: '';
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  background-color: #000000;
  opacity: .5;
  z-index: 100;
  transform: translateY(-100%);
  transition: all .5s;
}
.notesContent:hover::after {
  transform: translateY(0);
}
.notesLine {
  word-break: break-all;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  padding: 10px 20px;
}
</style>
