<template>
  <div class="function">
    <div class="fnInfo">
      <div v-for="(item, index) in fnData" :key="index" class="one">
        <img :src="item.img" alt="" />
        <div>
          <h6 v-for="(iten, inde) in item.title" :key="inde + 'a'">{{ iten }}</h6>
          <p v-if="item.desc" class="desc">{{ item.desc }}</p>
        </div>
      </div>
    </div>
    <div class="more">
      <a href="javascript:;">了解更多</a>
      |
      <a href="http://filseclab.com/documents/twister8tech_zh-cn.pdf">技术文档</a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    fnData: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss" scoped>
.function {
  width: 12rem;
  margin: auto;
  margin-top: .8rem;
}
.fnInfo{
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    font-size: 0;
    .one{
        width: 25%;
        display: flex;
        align-items: center;
        margin-bottom: .5rem;
        img{
            width: .6rem;
            margin-right: .2rem;
            &:hover{
                transition: all 1s;
                animation: myScale .6s 1;
            }
        }
        h6{
            font-size: .14rem;
            color: #333;
        }
        .desc{
            font-size: .12rem;
            color: #7d7d7d;
        }
    }
}
.more{
    color: #464646;
    font-size: .14rem;
    text-align: right;
    margin-bottom: .7rem;
    a{
        color: #e87f00;
    }
}
@keyframes myScale {
    0% {transform: scale(1,1)}
    50% {transform:scale(.8,.8)}
    100% {transform: scale(1,1)}
}
</style>