<template>
  <div class="we-container">
    <div class="we-title">周末去哪儿</div>
    <ul>
      <li class="we-product-item" v-for="item of weekendList" :key="item.id">
        <a class="we-fulllink" href="javascript:void(0)">
          <div class="product-imgcontainer">
            <img class="we-img" :src="item.imgUrl">
          </div>
          <div class="we-product-info">
            <p class="product-name">{{item.productName}}</p>
            <p class="product-desc">{{item.productDesc}}</p>
          </div>
        </a>
      </li>
    </ul>
    <div class="price-desc">
      <span class="iconfont hint-icon">&#xe622;</span>
      <p class="price-hint-info"><span class="hint-blod">票面价</span>是指通过景区指定窗口售卖的纸质门票上标注的价格</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  }
}
</script>

<style scoped>
  .we-title{height: .8rem;padding-left: .26rem;line-height: .8rem;color: #212121;background: #F5F5F5}
  .we-product-item{position: relative;margin-bottom: .1rem;background: #fff;}
  .we-fulllink{display: block;width: 100%;height: 100%;}
  .product-imgcontainer{overflow: hidden;width: 100%;height: 0;padding-bottom: 37.4375%}
  .we-img{width: 100%;}
  .we-product-info{position: relative;padding: .14rem .2rem .2rem .2rem;}
  .product-name{overflow: hidden;padding-right: 1.4rem;color: #212121;font-size: .28rem;line-height: .48rem;white-space: nowrap;text-overflow: ellipsis;}
  .product-desc{overflow: hidden;padding-right: 1.4rem;color: #616161;font-size: .24rem;line-height: .42rem;white-space: nowrap;text-overflow: ellipsis}
  .price-desc{margin-top: .1rem;padding: .14rem .1rem;font-size: .24rem;line-height: .32rem;background: #fff;color: #616161;}
  .hint-icon{width: .24rem;display: block;float: left;line-height: .32rem;font-size: .24rem;color: #616161;}
  .price-hint-info{margin-left: .3rem;}
  .hint-blod{font-weight: bold;}
</style>
