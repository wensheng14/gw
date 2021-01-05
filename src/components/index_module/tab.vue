<template>
  <div id="tab" class="w">
    <div class="tab-bar">
      <a
        href="javscript:;"
        v-for="(item, index) in items"
        :key="index"
        @mouseover="tab(index)"
        :class="{ red: index === curId }"
        >{{ item.item }}</a
      >
      <span>了解更多</span>
    </div>
    <div class="tab-con">
      <ul class="tab-Left" v-show="index === curId" v-for="(item,index) in contents" :key="index">
        <li  v-for="(item,index) in item" :key="index">
          <a href="#">{{item.item}}</a>
          <span>{{item.time}}</span>
        </li>
      </ul>
      <div class="tab-Right">
        <el-carousel height="150px">
          <el-carousel-item v-for="(item,index) in c" :key="index">
            <img :src="item.url" alt="" width="100%" height="100%">
            <!-- <p>{{item.title}}</p> -->
          </el-carousel-item>
        </el-carousel>
        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      curId: 0,
      items: [{ item: "学校要闻" }, { item: "学校新闻" }, { item: "技工动态" }],
      contents: [
        {
          content1: {
            item: '广州现疑似疯汉拿半米长刀 武警持枪戒备',
            time: '12-1',
          },
          content2: {
            item: '美国10位前防长发公开信：不支持特朗普翻转选举结果',
            time: '12-2',
          },
          content3: {
            item: '这是美国现在最热的话题 一盘特朗普的秘密录音带',
            time: '12-3',
          },
          content4: {
            item: '点赞！这对8岁双胞胎救下3岁落水小女孩 还不留名',
            time: '12-4',
          },
          content5: {
            item: '上四个月网课 拿几十万年薪？谁制造了芯片培训的狂',
            time: '12-5',
          },
        },
        {
          content1: {
            item: '有网友爆料称拼多多女员工下班路上猝死 公司尚未回',
            time: '12-1',
          },
          content2: {
            item: '盲目追求爆款的年代 我们该有怎样的"流量',
            time: '12-2',
          },
          content3: {
            item: '改变搜寻外星人的方式，从宇宙学角度定义生命！ GIF',
            time: '12-3',
          },
          content4: {
            item: '冬季必备手袋 像江浙沪女孩取时髦经',
            time: '12-4',
          },
          content5: {
            item: '呼伦贝尔这座城市太美了 迪拜潮只有Dunk联',
            time: '12-5',
          },
        },
        {
          content1: {
            item: '深圳现疑似疯汉拿半米长刀 武警持枪戒备',
            time: '12-1',
          },
          content2: {
            item: '广州现疑似疯汉拿半米长刀 武警持枪戒备',
            time: '12-2',
          },
          content3: {
            item: '广州现疑似疯汉拿半米长刀 武警持枪戒备',
            time: '12-3',
          },
          content4: {
            item: '广州现疑似疯汉拿半米长刀 武警持枪戒备',
            time: '12-4',
          },
          content5: {
            item: '广州现疑似疯汉拿半米长刀 武警持枪戒备',
            time: '12-5',
          },
        },
      ],
      c: [
        {
          url: require('../../assets/images/gg1.png'),
          title: '武警持枪戒备'
        },
        {
          url: require('../../assets/images/gg2.jpg'),
          title: '武警持枪戒备'
        },
      ]
    };
  },
  methods: {
    tab(index){
      this.curId = index;
    }
  },
};
</script>

<style>
#tab {
  width: 660px;
  height: 283px;
  background: #eee;
  color: #eee;
}

.tab-bar {
  width: 100%;
  height: 38px;
  line-height: 38px;
}
.tab-bar a {
  display: inline-block;
  width: 136px;
  height: 35px;
  line-height: 35px;
  font-size: 18px;
  color: #000;
  text-align: center;
  /* border-right: 3px solid #ddd; */
}
.tab-bar span {
  display: inline-block;
  width: 150px;
  height: 35px;
  line-height: 35px;
  font-size: 12px;
  color: #222;
  text-align: center;
  margin-left: 100px;
  cursor: pointer;
}
.tab-bar span:hover {
  color: #be2634;
}

.tab-con {
  display: flex;
  justify-content: space-between;
}
.tab-Left {
  width: 350px;
  padding: 10px;
}
.tab-Left li {
  display: flex;
  justify-content: space-between;
}
.tab-Left a {
  display: inline-block;
  width: 270px;
  height: 28px;
  line-height: 28px;
  font-size: 14px;
  color: #222;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}
.tab-Left a:hover {
  color: #be2634;
}
.tab-Left span {
  width: 33px;
  height: 28px;
  line-height: 28px;
  font-size: 12px;
}
.tab-Right {
  width: 240px;
  height: 180px;
  margin: 15px 50px 0 0;
}
.tab-Right p {
  width: 100%;
  height: 30px;
  line-height: 30px;
  text-align: center;
  font-size: 14px;
  color: #222;
  font-weight: 600;
}

.red {
  background-color: #be2635;
  color: #fff !important;
}
</style>