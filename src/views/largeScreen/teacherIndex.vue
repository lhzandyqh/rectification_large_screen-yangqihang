<template>
  <div class="all_container">
    <Header style="width: 100%;height: 12%" />
    <div style="width: 100%;height: 44%;">
      <div class="cure_container">
        <div class="cure_title">
          <div class="triangle-right" />
          <span>师资核心数据数据展示</span>
        </div>
        <div class="cure_table">
          <div class="table_head">
            <div class="table_head_one">
              <span>质控点说明</span>
            </div>
            <div class="table_head_two">
              <span>当前值</span>
            </div>
            <div class="table_head_three">
              <span>目标值</span>
            </div>
            <div class="table_head_four">
              <span>预警值</span>
            </div>
            <div class="table_head_five">
              <span>单位</span>
            </div>
          </div>
        </div>
        <vue-seamless-scroll :data="CardPartsStatisticsList" class="seamless-warp" :class-option="classOption">
          <ul class="table_ul">
            <li v-for="(item,index) in CardPartsStatisticsList" :key="index" class="DataList_top">
              <div class="DataList_top_one">
                <span>{{ item.name }}</span>
              </div>
              <div class="DataList_top_two">
                <span>{{ item.number }}</span>
              </div>
              <div class="DataList_top_three">
                <span>{{ item.targetNumber }}</span>
              </div>
              <div class="DataList_top_four">
                <span>{{ item.warnNumber }}</span>
              </div>
              <div class="DataList_top_five">
                <span>{{ item.danwei }}</span>
              </div>
            </li>
          </ul>
        </vue-seamless-scroll>
      </div>
      <div class="resource_container">
        <div class="resource_title">
          <div class="triangle-right-two" />
          <span>基础能力发展</span>
        </div>
        <div class="resource1_chart_container">
          <div class="resource1Chart">
            <div class="echart_container">
              <div id="resource1Chart" style="height: 100%;width: 100%;" />
            </div>
          </div>
        </div>
      </div>
      <div class="resource2_container">
        <!--        <div class="resource2_title">-->
        <!--          <div class="triangle-right-three" />-->
        <!--          <span>学生管理能力</span>-->
        <!--        </div>-->
        <div class="show_card_container_one">
          <div class="left_icon_container_one">
            <img src="../../assets/icon/fudaoyuan2.png">
          </div>
          <div class="right_text_container_one">
            <div class="text_header_one">
              <span>承担辅导员数量</span>
            </div>
            <div class="number_container_one">
              <span>89</span>
            </div>
          </div>
        </div>
        <div class="show_card_container_one">
          <div class="left_icon_container_one">
            <img src="../../assets/icon/shetuan2.png">
          </div>
          <div class="right_text_container_one">
            <div class="text_header_one">
              <span>学生社团数量</span>
            </div>
            <div class="number_container_one">
              <span>120</span>
            </div>
          </div>
        </div>
        <div class="show_card_container_one">
          <div class="left_icon_container_one">
            <img src="../../assets/icon/xuesheng2.png">
          </div>
          <div class="right_text_container_one">
            <div class="text_header_one">
              <span>帮扶学生数量</span>
            </div>
            <div class="number_container_one">
              <span>123</span>
            </div>
          </div>
        </div>
      </div>
      <div class="resource3_container">
        <div class="resource3_title">
          <div class="triangle-right-four" />
          <span>教学专业能力</span>
        </div>
        <div class="resource3_chart_container">
          <div class="resource3Chart1">
            <div class="show_card_container_two">
              <div class="left_icon_container_two">
                <img src="../../assets/icon/kechengshu.png">
              </div>
              <div class="right_text_container_two">
                <div class="text_header_two">
                  <span>课程数</span>
                </div>
                <div class="number_container_two">
                  <span>82</span>
                </div>
              </div>
            </div>
            <div class="show_card_container_two">
              <div class="left_icon_container_two">
                <img src="../../assets/icon/zhoukeshi.png">
              </div>
              <div class="right_text_container_two">
                <div class="text_header_two">
                  <span>周课时</span>
                </div>
                <div class="number_container_two">
                  <span>90</span>
                </div>
              </div>
            </div>
            <div class="show_card_container_two">
              <div class="left_icon_container_two">
                <img src="../../assets/icon/banjishu.png">
              </div>
              <div class="right_text_container_two">
                <div class="text_header_two">
                  <span>任课班级数</span>
                </div>
                <div class="number_container_two">
                  <span>88</span>
                </div>
              </div>
            </div>
            <div class="show_card_container_two">
              <div class="left_icon_container_two">
                <img src="../../assets/icon/xueshengshu.png">
              </div>
              <div class="right_text_container_two">
                <div class="text_header_two">
                  <span>任课学生数</span>
                </div>
                <div class="number_container_two">
                  <span>82</span>
                </div>
              </div>
            </div>
            <div class="show_card_container_two">
              <div class="left_icon_container_two">
                <img src="../../assets/icon/daokelv.png">
              </div>
              <div class="right_text_container_two">
                <div class="text_header_two">
                  <span>学生到课率</span>
                </div>
                <div class="number_container_two">
                  <span>90</span>
                </div>
              </div>
            </div>
            <div class="show_card_container_two">
              <div class="left_icon_container_two">
                <img src="../../assets/icon/dudaopingjia.png">
              </div>
              <div class="right_text_container_two">
                <div class="text_header_two">
                  <span>督导评价分数</span>
                </div>
                <div class="number_container_two">
                  <span>88</span>
                </div>
              </div>
            </div>
            <div class="show_card_container_two">
              <div class="left_icon_container_two">
                <img src="../../assets/icon/xueshengpingjia.png">
              </div>
              <div class="right_text_container_two">
                <div class="text_header_two">
                  <span>学生评价分数</span>
                </div>
                <div class="number_container_two">
                  <span>88</span>
                </div>
              </div>
            </div>
          </div>
          <div class="resource3Chart2">
            <div class="echart_container">
              <div id="resource3ChartTwo" style="height: 100%;width: 100%" />
            </div>
          </div>
        </div>
      </div>
      <div class="resource4_container">
        <div class="resource4_title">
          <div class="triangle-right-five" />
          <span>科研与社会服务能力</span>
        </div>
        <div class="resource4_chart_container">
          <div class="resource4Chart1">
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/keti31.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>主持纵向课题到款额</span>
                </div>
                <div class="number_container">
                  <span>230000</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/keti32.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>参与纵向课题到款额</span>
                </div>
                <div class="number_container">
                  <span>350000</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/keti33.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>主持横向课题到款额</span>
                </div>
                <div class="number_container">
                  <span>920000</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/keti34.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>参与横向课题到款额</span>
                </div>
                <div class="number_container">
                  <span>1560000</span>
                </div>
              </div>
            </div>
          </div>
          <div class="resource4Chart2">
            <div class="echart_container">
              <div id="resource4ChartTwo" style="height: 100%;width: 100%;" />
            </div>
          </div>
          <div class="resource4Chart3">
            <div class="echart_container">
              <div id="resource4ChartThree" style="height: 100%;width: 100%;" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/views/myComponents/head/teaheader'
import vueSeamlessScroll from 'vue-seamless-scroll'
// import * as echarts from 'echarts'
export default {
  name: 'TeacherIndex',
  components: {
    Header,
    vueSeamlessScroll
  },
  data() {
    return {
      CardPartsStatisticsList: [
        {
          name: '师资总数',
          number: '167',
          targetNumber: '200',
          warnNumber: '120',
          danwei: '人'
        },
        {
          name: '双师素质教师',
          number: '52',
          targetNumber: '120',
          warnNumber: '60',
          danwei: '人'
        },
        {
          name: '骨干教师',
          number: '68',
          targetNumber: '114',
          warnNumber: '45',
          danwei: '人'
        },
        {
          name: '专业带头人',
          number: '17',
          targetNumber: '22',
          warnNumber: '10',
          danwei: '人'
        },
        {
          name: '年度考核平均分',
          number: '89',
          targetNumber: '95',
          warnNumber: '70',
          danwei: '分'
        },
        {
          name: '师德考核平均分',
          number: '95',
          targetNumber: '98',
          warnNumber: '80',
          danwei: '分'
        },
        {
          name: '督导评价平均分',
          number: '90',
          targetNumber: '95',
          warnNumber: '80',
          danwei: '分'
        },
        {
          name: '学生评价平均分',
          number: '96',
          targetNumber: '95',
          warnNumber: '80',
          danwei: '分'
        },
        {
          name: '教学事故数',
          number: '1',
          targetNumber: '0',
          warnNumber: '2',
          danwei: '次'
        }
      ]
    }
  },
  computed: {
    classOption() {
      return {
        step: 0.2, // 数值越大速度滚动越快
        limitMoveNum: 6, // 开始无缝滚动的数据量 this.dataList.length
        hoverStop: true, // 是否开启鼠标悬停stop
        direction: 1, // 0向下 1向上 2向左 3向右
        openWatch: true, // 开启数据实时监控刷新dom
        singleHeight: 0, // 单步运动停止的高度(默认值0是无缝不停止的滚动) direction => 0/1
        singleWidth: 0, // 单步运动停止的宽度(默认值0是无缝不停止的滚动) direction => 2/3
        waitTime: 1000 // 单步运动停止的时间(默认值1000ms)
      }
    }
  },
  mounted() {
    this.initResource1()
    this.resourceRes1()
    this.initResource32()
    this.resourceRes32()
    this.initResource42()
    this.resourceRes42()
    this.initResource43()
    this.resourceRes43()
  },
  methods: {
    initResource1() {
      console.log('生成资源图1')
      // var resource1Chart = document.getElementById('resource1Chart')
      var resource1Chart = this.$echarts.init(document.getElementById('resource1Chart'), 'light')
      this.resource1Chart = resource1Chart
      // var testChart1 = echarts.init(resource1Chart)
      var optionArray = [{
        title: {
          text: '证书获取',
          top: '0',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        legend: {
          top: '5%',
          left: 'center'
        },
        series: [
          {
            name: '证书获取',
            type: 'pie',
            radius: ['40%', '70%'],
            avoidLabelOverlap: false,
            itemStyle: {
              borderRadius: 10,
              borderColor: '#fff',
              borderWidth: 2
            },
            label: {
              show: false,
              position: 'center'
            },
            emphasis: {
              label: {
                show: true,
                fontSize: '23',
                fontWeight: 'bold'
              }
            },
            labelLine: {
              show: false
            },
            data: [
              { value: 1048, name: '高校教师资格证' },
              { value: 735, name: '职业（执业）资格证书' },
              { value: 580, name: '其他' }
            ]
          }
        ]
      },
      {
        title: {
          text: '继续教育与培训',
          top: '0',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        legend: {
          top: '5%',
          left: 'center'
        },
        series: [
          {
            name: '继续教育与培训',
            type: 'pie',
            radius: ['40%', '70%'],
            avoidLabelOverlap: false,
            label: {
              show: false,
              position: 'center'
            },
            emphasis: {
              label: {
                show: true,
                fontSize: '23',
                fontWeight: 'bold'
              }
            },
            labelLine: {
              show: false
            },
            data: [
              { value: 1002, name: '学历提升' },
              { value: 156, name: '培训' },
              { value: 654, name: '进修' },
              { value: 266, name: '企业实践' },
              { value: 356, name: '社会兼职' },
              { value: 700, name: '其他' }
            ]
          }
        ]
      }]
      this.resource1Chart.setOption(optionArray[0])
      // setTimeout(() => {
      //   this.testBingChart.setOption(option2)
      // }, 2000)
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource1Chart.setOption(optionArray[i])
      }, 3000)
    },
    resourceRes1() {
      console.log('资源图1变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource1Chart').offsetWidth
        const h = document.getElementById('resource1Chart').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource1Chart.resize(resize)
        }, 100)
      })
    },
    initResource32() {
      console.log('生成专业资源图4')
      var resource3ChartTwo = this.$echarts.init(document.getElementById('resource3ChartTwo'), 'light')
      // this.testChart = this.$echarts.init(document.getElementById('testChart'), 'light')
      this.resource3ChartTwo = resource3ChartTwo
      var option

      var data = [{
        name: '教学能力比赛获奖',
        children: [{
          name: '院级',
          value: 15
        }, {
          name: '省级',
          value: 4
        }, {
          name: '国家级',
          value: 5
        }]
      }, {
        name: '专业技能竞赛获奖',
        children: [{
          name: '院级',
          value: 15
        }, {
          name: '省级',
          value: 4
        }, {
          name: '国家级',
          value: 5
        }]
      }, {
        name: '教学质量工程获奖',
        children: [{
          name: '院级',
          value: 15
        }, {
          name: '省级',
          value: 4
        }, {
          name: '国家级',
          value: 5
        }]
      }, {
        name: '参与专业建设数量',
        value: 5
      }, {
        name: '参与课程建设数量',
        value: 15
      }, {
        name: '参与重大工程数量',
        value: 15
      }, {
        name: '参与实训基地建设数量',
        value: 15
      }, {
        name: '主持教研项目数量',
        children: [{
          name: '院级',
          value: 15
        }, {
          name: '省级',
          value: 4
        }, {
          name: '国家级',
          value: 5
        }]
      }, {
        name: '参与教研项目数量',
        children: [{
          name: '院级',
          value: 15
        }, {
          name: '省级',
          value: 4
        }, {
          name: '国家级',
          value: 5
        }]
      }, {
        name: '主编教材数量',
        children: [{
          name: '校本教材',
          value: 15
        }, {
          name: '普通公开出版教材',
          value: 4
        }, {
          name: '国家规划教材',
          value: 5
        }]
      }, {
        name: '参编教材数量',
        children: [{
          name: '校本教材',
          value: 15
        }, {
          name: '普通公开出版教材',
          value: 4
        }, {
          name: '国家规划教材',
          value: 5
        }]
      }]

      option = {
        series: {
          type: 'sunburst',
          data: data,
          radius: [60, '90%'],
          itemStyle: {
            borderRadius: 10,
            borderWidth: 2
          },
          label: {
            show: true
          }
        }
      }

      this.resource3ChartTwo.setOption(option)
    },
    resourceRes32() {
      console.log('专业资源图变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource3ChartTwo').offsetWidth
        const h = document.getElementById('resource3ChartTwo').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource3ChartTwo.resize(resize)
        }, 100)
      })
    },
    initResource42() {
      console.log('生成专业资源图4')
      var resource4ChartTwo = this.$echarts.init(document.getElementById('resource4ChartTwo'), 'light')
      // this.testChart = this.$echarts.init(document.getElementById('testChart'), 'light')
      this.resource4ChartTwo = resource4ChartTwo
      var option =
      {
        title: {
          text: '课题数量图'
        },
        legend: {},
        tooltip: {},
        dataset: {
          source: [
            ['product', '院级', '省级', '国家级'],
            ['主持纵向课题数量', 43, 85, 100],
            ['参与纵向课题数量', 43, 85, 100],
            ['主持横向课题数量', 43, 85, 100],
            ['参与横向课题数量', 43, 85, 100]
          ]
        },
        xAxis: { type: 'category' },
        yAxis: {
          type: 'value',
          scale: true,
          name: '数量',
          max: 200,
          min: 0,
          boundaryGap: [0.2, 0.2]
        },
        series: [
          { type: 'bar' },
          { type: 'bar' },
          { type: 'bar' }
        ]
      }
      this.resource4ChartTwo.setOption(option)
    },
    resourceRes42() {
      console.log('专业资源图变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource4ChartTwo').offsetWidth
        const h = document.getElementById('resource4ChartTwo').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource4ChartTwo.resize(resize)
        }, 100)
      })
    },
    initResource43() {
      console.log('生成专业资源图')
      this.resource4ChartThree = this.$echarts.init(document.getElementById('resource4ChartThree'), 'light')
      var optionArray = [{
        title: {
          text: '发表论文数量',
          top: '0',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        legend: {
          top: '7%',
          left: 'center'
        },
        series: [
          {
            name: '发表论文数量',
            type: 'pie',
            radius: ['40%', '70%'],
            avoidLabelOverlap: false,
            label: {
              show: false,
              position: 'center'
            },
            emphasis: {
              label: {
                show: true,
                fontSize: '23',
                fontWeight: 'bold'
              }
            },
            labelLine: {
              show: false
            },
            data: [
              { value: 1048, name: '普通期刊' },
              { value: 735, name: '中文核心期刊' },
              { value: 580, name: 'SCI' },
              { value: 735, name: 'EI等' }
            ]
          }
        ]
      }, {
        title: {
          text: '出版专著数量',
          top: '0',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        legend: {
          top: '7%',
          left: 'center'
        },
        series: [
          {
            name: '出版专著数量',
            type: 'pie',
            radius: ['40%', '70%'],
            avoidLabelOverlap: false,
            label: {
              show: false,
              position: 'center'
            },
            emphasis: {
              label: {
                show: true,
                fontSize: '23',
                fontWeight: 'bold'
              }
            },
            labelLine: {
              show: false
            },
            data: [
              { value: 1002, name: '主编' },
              { value: 654, name: '参编' }
            ]
          }
        ]
      }, {
        title: {
          text: '专利数量',
          top: '0',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        legend: {
          top: '7%',
          left: 'center'
        },
        series: [
          {
            name: '专利数量',
            type: 'pie',
            radius: ['40%', '70%'],
            avoidLabelOverlap: false,
            label: {
              show: false,
              position: 'center'
            },
            emphasis: {
              label: {
                show: true,
                fontSize: '23',
                fontWeight: 'bold'
              }
            },
            labelLine: {
              show: false
            },
            data: [
              { value: 865, name: '发明专利' },
              { value: 752, name: '实用新型专利' },
              { value: 693, name: '外观专利' },
              { value: 472, name: '软件著作权' }
            ]
          }
        ]
      }]
      this.resource4ChartThree.setOption(optionArray[0])
      // setTimeout(() => {
      //   this.testBingChart.setOption(option2)
      // }, 2000)
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource4ChartThree.setOption(optionArray[i])
      }, 3000)
    },
    resourceRes43() {
      console.log('专业资源图变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource4ChartThree').offsetWidth
        const h = document.getElementById('resource4ChartThree').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource4ChartThree.resize(resize)
        }, 100)
      })
    }
  }
}
</script>

<style scoped>
.all_container {
  /*background-color: pink;*/
  width: 100%;
  height: 100%;
  position: relative;
}
.title{
  font-size: 1rem;
  font-weight: bold;
}
.chartBox {
  /*margin-top: 0.5rem;*/
  /*margin-left: 1rem;*/
  width: 30%;
  height: 100%;
  display: inline-block;
  /*width:calc(100vh / 3*2 - 1.8rem);*/
  /*height: calc(70vh / 3*2 - 1.8rem);*/
  /*background-color: skyblue;*/
}
.echart_container {
  width: 100%;
  /*height: calc(70vh / 3*2 - 1.8rem);*/
  height: 100%;
}
.cure_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.echart_container {
  width: 100%;
  /*height: calc(70vh / 3*2 - 1.8rem);*/
  height: 100%;
}
.cure_title {
  margin-left: 1rem;
  padding-top: 1rem;
}

.cure_container {
  /*display: inline-block;*/
  float: left;
  width: 33%;
  height: 100%;
  /*background-color: skyblue;*/
}
.triangle-right {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #00ff37;
  border-bottom: 0.5rem solid transparent;
}
.cure_title span {
  font-size: 1rem;
  display: inline-block;
  margin-left: 0.5rem;
  color: #6b7179;
}
.seamless-warp{
  width: 100%;
  /*height: calc(50% - 1rem);*/
  height: 70%;
  overflow: hidden;
}
.table_head {
  margin-top: 1rem;
  height: 2.5rem;
  width: 90%;
  background-color: #c9c9c9;
  margin-left: 5%;
}
.table_head_one {
  height: 2.5rem;
  width: 40%;
  float: left;
}
.table_head_one span {
  margin-left: 2rem;
  line-height: 2.5rem;
  color: white;
}
.table_head_two {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.table_head_two span {
  line-height: 2.5rem;
  color: white;
}
.table_head_three {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.table_head_four {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.table_head_four span {
  line-height: 2.5rem;
  color: white;
}
.table_head_five {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.table_head_five span {
  line-height: 2.5rem;
  color: white;
}
.table_head_three span {
  line-height: 2.5rem;
  color: white;
}
.seamless-warp ul li {
  background-color: #f1f0f0;
  margin-left: -0.3rem;
  height: 2.5rem;
  width: 95%;
  margin-top: 0.8rem;
}
.table_ul li {
  list-style-type: none;
}
.DataList_top {
  height: 2.5rem;
  width: 95%;
}
.DataList_top_one {
  height: 2.5rem;
  width: 40%;
  float: left;
}
.DataList_top_one span {
  margin-left: 2rem;
  line-height: 2.5rem;
  color: #6c6969;
}
.DataList_top_one {
  height: 2.5rem;
  width: 40%;
  float: left;
}
.DataList_top_two {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.DataList_top_two span {
  /*margin-left: -2rem;*/
  line-height: 2.5rem;
  color: #6c6969;
}
.DataList_top_three {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.DataList_top_three span {
  /*margin-left: 2rem;*/
  line-height: 2.5rem;
  color: #6c6969;
}
.DataList_top_four {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.DataList_top_four span {
  /*margin-left: 2rem;*/
  line-height: 2.5rem;
  color: #6c6969;
}
.DataList_top_five {
  height: 2.5rem;
  width: 15%;
  float: left;
}
.DataList_top_five span {
  /*margin-left: 2rem;*/
  line-height: 2.5rem;
  color: #6c6969;
}
.resource_container {
  width: 40%;
  height: 100%;
  float: left;
  /*background-color: skyblue;*/
}
.resource_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.resource_title span {
  font-size: 1rem;
  display: inline-block;
  margin-left: 0.5rem;
  color: #6b7179;
}
.triangle-right-two {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #8000ff;
  border-bottom: 0.5rem solid transparent;
}
.resource1_chart_container {
  width: 100%;
  height: 88%;
  /*background: #5dd61b;*/
}
.resource1Chart {
  width: 100%;
  height: 100%;
}
.resource2_container {
  float: left;
  width: 27%;
  height: 100%;
  /*background-color: skyblue;*/
}
.resource2_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.resource2_title span {
  font-size: 1rem;
  display: inline-block;
  margin-left: 0.5rem;
  color: #6b7179;
}
.triangle-right-three {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #0a15e5;
  border-bottom: 0.5rem solid transparent;
}
.resource2_chart_container {
  width: 100%;
  height: 88%;
  /*background: #8c939d;*/
}
.resource2Chart {
  width: 100%;
  height: 100%;
}
.resource3_container {
  float: left;
  width: 40%;
  height: 100%;
  /*background-color: skyblue;*/
}
.resource3_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.resource3_title span {
  font-size: 1rem;
  display: inline-block;
  margin-left: 0.5rem;
  color: #6b7179;
}
.triangle-right-four {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #dd146a;
  border-bottom: 0.5rem solid transparent;
}
.resource3_chart_container {
  width: 100%;
  height: 88%;
  /*background: #8c939d;*/
}
.resource3Chart1 {
  width: 30%;
  height: 100%;
  float: left;
  display: inline-block;
  /*background: #105fcf;*/
}
.resource3Chart2 {
  width: 70%;
  height: 100%;
  float: left;
  display: inline-block;
  /*background: #16d936;*/
}
.resource4_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.resource4_title span {
  font-size: 1rem;
  display: inline-block;
  margin-left: 0.5rem;
  color: #6b7179;
}
.triangle-right-five {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #0feee6;
  border-bottom: 0.5rem solid transparent;
}
.resource4_chart_container {
  width: 100%;
  height: 88%;
  /*background: #8c939d;*/
}
.resource4Chart1 {
  width: 100%;
  height: 30%;
  float: left;
  /*background: #1a6adb;*/
}
.resource4Chart2 {
  width: 70%;
  height: 70%;
  float: left;
  /*background: #741adb;*/
}
.resource4Chart3 {
  width: 30%;
  height: 70%;
  float: left;
  /*background: #b140d9;*/
}
.resource4_container {
  float: left;
  width: 60%;
  height: 100%;
  /*background-color: #22b0ea;*/
}
.show_card_container_one {
  width: 90%;
  height: 31%;
  border-radius: 1rem;
  background: white;
  margin-bottom: 2%;
  /*margin-top: 3%;*/
  box-shadow: 0.2rem 0.2rem 0.1rem #cecdcd;
}
.left_icon_container_one {
  float: left;
  height: 100%;
  width: 30%;
  /*background: green;*/
  background: deepskyblue;
  border-radius: 1rem 0 0 1rem;
  text-align: center;
}
.left_icon_container_one img {
  width: 60%;
  height: 60%;
  margin-top: 20%;
}
.right_text_container_one {
  float: left;
  display: inline-block;
  height: 100%;
  width: 60%;
  border-radius: 0 1rem 1rem 0;
  /*background-color: pink;*/
}
.text_header_one {
  width: 100%;
  height: 40%;
  /*background-color: #0a76a4;*/
  text-align: center;
  margin-top: 10%;
}
.text_header_one span {
  color: #48494b;
  font-weight: bold;
  font-size: 1.3rem;
}
.number_container_one {
  text-align: center;
  margin-top: -5%;
}
.number_container_one span {
  font-size: 1.8rem;
  font-weight: bold;
  color: #4dbae7;
}
.show_card_container_two {
  float: right;
  width: 93%;
  height: 13%;
  border-radius: 3rem;
  background: white;
  margin-bottom: 1%;
  box-shadow: 0.2rem 0.2rem 0.1rem #cecdcd;
}
.left_icon_container_two {
  float: left;
  height: 100%;
  width: 30%;
  /*background: green;*/
  background: deepskyblue;
  border-radius: 3rem 0 0 3rem;
  text-align: center;
}
.left_icon_container_two img {
  width: 60%;
  height: 60%;
  margin-top: 15%;
}
.right_text_container_two {
  float: left;
  display: inline-block;
  height: 100%;
  width: 60%;
  border-radius: 0 1rem 1rem 0;
  /*background-color: pink;*/
}
.text_header_two {
  width: 100%;
  height: 40%;
  /*background-color: #0a76a4;*/
  text-align: center;
  margin-top: 5%;
}
.text_header_two span {
  color: #48494b;
  font-weight: bold;
  font-size: 1.0rem;
}
.number_container_two {
  text-align: center;
  margin-top: -2%;
}
.number_container_two span {
  font-size: 1.2rem;
  font-weight: bold;
  color: #4dbae7;
}
.show_card_container {
  float: left;
  width: 23%;
  height: 70%;
  margin-top: 1.5%;
  margin-right: 1%;
  /*display: inline-block;*/
  border-radius: 1rem;
  background: white;
  box-shadow: 0.2rem 0.2rem 0.1rem #cecdcd;
}
.left_icon_container {
  float: left;
  height: 100%;
  width: 40%;
  /*background: green;*/
  background: deepskyblue;
  border-radius: 1rem 0 0 1rem;
  text-align: center;
}
.left_icon_container img {
  width: 50%;
  height: 70%;
  margin-top: 10%;
}
.right_text_container {
  float: left;
  display: inline-block;
  height: 100%;
  width: 60%;
  border-radius: 0 1rem 1rem 0;
  /*background-color: pink;*/
}
.text_header {
  width: 100%;
  height: 40%;
  /*background-color: #0a76a4;*/
  text-align: center;
  margin-top: 10%;
}
.text_header span {
  color: #48494b;
  font-weight: bold;
  font-size: 1.0rem;
}
.number_container {
  text-align: center;
  margin-top: -5%;
}
.number_container span {
  font-size: 1.5rem;
  font-weight: bold;
  color: #4dbae7;
}
</style>
