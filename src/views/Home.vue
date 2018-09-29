+<template>
  <div>
    <!-- 顶上的蓝线 -->
    <div class="border-blue"></div>
    <div>
      <div class="width-1000">
        <span class="font-12 float-left">您好，欢迎来到广州可德机械设备有限公司官方网站！</span>
        <div class="float-right">
          <a>中文</a>
          <a>English</a>
        </div>
        <div class="clear"></div>
        <div class="float-left padding-top-20">
          <img src="../assets/images/logo.png">
        </div>
        <div class="float-right tel">
          <span class="block color-blue font-16">咨询热线</span>
          <span class="block font-20 font-weight-bolder">13806272829</span>
        </div>
        <div class="clear"></div>
      </div>
      <div class="background-blue" align="center">
        <el-menu
                :default-active="activeIndex"
                class="width-1000"
                mode="horizontal"
                @select="handleSelect"
                background-color="#409EFF"
                text-color="#fff"
                active-text-color="#fff">
          <el-menu-item index="1" class="font-16 width-124">网站首页</el-menu-item>
          <el-menu-item index="2" class="font-16 width-124">关于可德</el-menu-item>
          <el-menu-item index="3" class="font-16 width-124">荣誉资质</el-menu-item>
          <el-menu-item index="4" class="font-16 width-124">产品中心</el-menu-item>
          <el-menu-item index="5" class="font-16 width-124">新闻资讯</el-menu-item>
          <el-menu-item index="6" class="font-16 width-124">工程案例</el-menu-item>
          <el-menu-item index="7" class="font-16 width-124">在线留言</el-menu-item>
          <el-menu-item index="8" class="font-16 width-124">联系方式</el-menu-item>
        </el-menu>
      </div>
      <div class="block">
        <el-carousel height="500px">
          <el-carousel-item v-for="item in carousels" :key="item.id">
            <img class="carousel-img" :src="item.idView">
          </el-carousel-item>
        </el-carousel>
      </div>
      <div class="block background-grey height-60">
        <div class="width-1000">
          <div class="float-left padding-top-15">
            <span class="font-weight-bolder">热门关键字：</span>
            <span class="font-14 key-word" v-for="key in hotKeys" :key="key.value">
              <a>{{key.value}}</a>
            </span>
          </div>
          <div class="float-right width-400 background-black padding-10 height-40">
            <el-input placeholder="请输入搜索内容" v-model="searchKey" class="width-350">
              <el-button slot="append" icon="el-icon-search"></el-button>
            </el-input>
          </div>
          <div class="clear"></div>
        </div>
      </div>
      <div class="grey-shadow">
        <div class="width-1000 shadow-back border-blue">
          <span class="introduce-title">可德机械专注生产烘焙设备</span>
          <span class="introduce-small-title">热销产品</span>
          <div >
            <a class="left"></a>
            <a class="right"></a>
            <div class="" style="height: 280px">
              <ul>
                <li>
                  <img src=""/>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="publicize">
        <div class="publicize-title">
          <h1>优质产品，源于我们的与众不同</h1>
        </div>
        <div class="publicize-small-title">
          <span>--------------------------------------------------------------------------&nbsp;&nbsp;&nbsp;&nbsp;FOUR MAJOR ADVANTAGES&nbsp;&nbsp;&nbsp;&nbsp;--------------------------------------------------------------------------</span>
        </div>
        <div class="publicize-inner">
          <div class="publicize-item" v-for="item in adItems" :key="item.id">
            <img :src="item.img"/>
            <h2> {{item.title}} </h2>
            <p> {{item.content}} </p>
          </div>
        </div>
        <div class="clear"></div>
      </div>
      <div class="publicize-bottom">
        <!-- <img src="../assets/images/adbottom.jpg"> -->
      </div>
      <div class="case">
        <h1 class="big-title">科技烘焙，火力美食</h1>
        <span class="small-title">走进可德机械，见证我们做过的案例</span>
        <div class="more">
          <a>
            <h2>查看更多</h2>
          </a>
        </div>
        <div class="product-case">
          <div class="product-border" v-for="item in productItems" :key="item.id">
            <img :src="item.img"/>
            <span> {{item.title}} </span>
          </div>
          <div class="clear"></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { slider, slideritem } from 'vue-concise-slider'// import slider components
export default {
  name: 'home',
  data () {
    return {
      activeIndex: '1',
      carousels: [{
        id: 0, idView: require('../assets/images/carousel1.jpg')
      }, {
        id: 1, idView: require('../assets/images/carousel2.jpg')
      }],
      hotKeys: [{
        value: '鲜奶搅拌机'
      }, {
        value: '齿轮搅拌机'
      }, {
        value: '和面机'
      }, {
        value: '揉压面机'
      }],
      searchKey: '',
      adItems: [{
        id: 0,
        img: require('../assets/images/adpic1.png'),
        title: '因地制宜，个性定制',
        content: '以专业生产、销售为主的企业，因地制宜，具有为客户工厂规划、设计的能力，根据客户需求量身定制，提供专业的设备方案。'
      }, {
        id: 1,
        img: require('../assets/images/adpic2.png'),
        title: '先进技术，品质保证',
        content: '公司引进欧美的先进技术，拥有高素质的设计制造专业人才，视产品质量为公司命脉，努力搭建行业战略合作联盟和行业交流平台。'
      }, {
        id: 2,
        img: require('../assets/images/adpic3.png'),
        title: '精益求精质量服务',
        content: '完善的服务体制，始终坚持以客户为中心，客户是上帝的服务意识为宗旨，用心经营，让客户满意。'
      }, {
        id: 3,
        img: require('../assets/images/adpic4.png'),
        title: '简洁大方，功能齐全',
        content: '外形简约、美观大方，功能结构合理、耐用，产品品种齐全，并拥有多项技术。'
      }],
      productItems: [{
        id: 0,
        img: require('../assets/images/foreginCase.jpg'),
        title: '国内案例'
      }, {
        id: 1,
        img: require('../assets/images/foreginCase.jpg'),
        title: '国外案例'
      }]
    }
  },
  components: {
    slider,
    slideritem
  },
  mounted () {

  },
  methods: {
    handleSelect () {

    }
  }
}
</script>
<style lang='less' rel='stylesheet/less' scoped>
  @import 'home.less';
</style>
