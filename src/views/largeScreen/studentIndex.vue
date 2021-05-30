<template>
  <div class="all_container">
    <Header style="width: 100%;height: 12%" />
    <div class="container1">
      <div style="width: 100%;height: 50%;">
        <div class="cure_container">
          <div class="cure_title">
            <div class="triangle-right" />
            <span>学生基本信息</span>
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
        <div class="resource1_container">
          <div class="resource1_title">
            <div class="triangle-right-one" />
            <span>行为习惯</span>
          </div>
          <div class="resource1_chart_container">
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/habit1.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>处分次数</span>
                </div>
                <div class="number_container">
                  <span>92</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/habit2.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>夜不归宿次数</span>
                </div>
                <div class="number_container">
                  <span>249</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/habit3.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>宿舍卫生通报次数</span>
                </div>
                <div class="number_container">
                  <span>120</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/habit4.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>图书借阅量</span>
                </div>
                <div class="number_container">
                  <span>4139</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/habit5.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>日均上网时长</span>
                </div>
                <div class="number_container">
                  <span>8h</span>
                </div>
              </div>
            </div>
            <div class="show_card_container">
              <div class="left_icon_container">
                <img src="../../assets/icon/habit6.png">
              </div>
              <div class="right_text_container">
                <div class="text_header">
                  <span>勤工助学时长</span>
                </div>
                <div class="number_container">
                  <span>2h</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container2">
      <div class="resource2_title">
        <div class="triangle-right-two" />
        <span>学业发展</span>
      </div>
      <!--      <div class="container21">-->
      <!--        <div class="resource2_title">-->
      <!--          <div class="triangle-right-four" />-->
      <!--          <span>教学专业能力</span>-->
      <!--        </div>-->
      <!--      </div>-->
      <div class="container22">
        <div class="echart_container">
          <div id="resource2Chart" style="height: 100%;width: 100%;" />
        </div>
      </div>
      <div class="container23">
        <div class="container23_layer1">
          <div class="stuChartOne">
            <div class="containerChart1">
              <div class="echart_container">
                <div id="resource3Chart1" style="height: 100%;width: 100%;" />
              </div>
            </div>
          </div>
          <div class="stuChartOne">
            <div class="containerChart2">
              <div class="echart_container">
                <div id="resource3Chart2" style="height: 100%;width: 100%;" />
              </div>
            </div>
          </div>
        </div>
        <div class="container23_layer2">
          <div class="stuChartTwo">
            <div class="containerChart1">
              <div class="echart_container">
                <div id="resource3Chart3" style="height: 100%;width: 100%;" />
              </div>
            </div>
          </div>
          <div class="stuChartTwo">
            <div class="containerChart2">
              <div class="echart_container">
                <div id="resource3Chart4" style="height: 100%;width: 100%;" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container3">
      <div class="resource3_title">
        <div class="triangle-right-three" />
        <span>发展性素质</span>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi1.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>体测成绩</span>
          </div>
          <div class="number_container_two">
            <span>82</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi2.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>心理素质测评分</span>
          </div>
          <div class="number_container_two">
            <span>90</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi3.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>文体比赛获奖</span>
          </div>
          <div class="number_container_two">
            <span>100</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi4.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>创新创业获奖</span>
          </div>
          <div class="number_container_two">
            <span>190</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi5.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>技能比赛获奖</span>
          </div>
          <div class="number_container_two">
            <span>230</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi6.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>基础性学科获奖</span>
          </div>
          <div class="number_container_two">
            <span>86</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi7.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>其他获奖</span>
          </div>
          <div class="number_container_two">
            <span>90</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi8.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>加入社团数量</span>
          </div>
          <div class="number_container_two">
            <span>200</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi9.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>参加各类讲座数量</span>
          </div>
          <div class="number_container_two">
            <span>123</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi10.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>参与社会活动数量</span>
          </div>
          <div class="number_container_two">
            <span>90</span>
          </div>
        </div>
      </div>
      <div class="show_card_container_two">
        <div class="left_icon_container_two">
          <img src="../../assets/icon/suzhi11.png">
        </div>
        <div class="right_text_container_two">
          <div class="text_header_two">
            <span>其他证（照）考取数量</span>
          </div>
          <div class="number_container_two">
            <span>90</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/views/myComponents/head/stuheader'
import vueSeamlessScroll from 'vue-seamless-scroll'

export default {
  name: 'StudentIndex',
  components: {
    Header,
    vueSeamlessScroll
  },
  data() {
    return {
      CardPartsStatisticsList: [
        {
          name: '在校生数量',
          number: '22432',
          targetNumber: '26000',
          warnNumber: '22000',
          danwei: '人'
        },
        {
          name: '优秀学生数量',
          number: '560',
          targetNumber: '600',
          warnNumber: '320',
          danwei: '人'
        },
        {
          name: '日均消费金额',
          number: '41',
          targetNumber: '30',
          warnNumber: '50',
          danwei: 'RMB'
        },
        {
          name: '日均上网时间',
          number: '7',
          targetNumber: '4',
          warnNumber: '10',
          danwei: '小时'
        },
        {
          name: '心理素质测评分',
          number: '91',
          targetNumber: '95',
          warnNumber: '80',
          danwei: '分'
        },
        {
          name: '体测平均成绩',
          number: '92',
          targetNumber: '95',
          warnNumber: '85',
          danwei: '分'
        },
        {
          name: '平均就业率',
          number: '96',
          targetNumber: '100',
          warnNumber: '90',
          danwei: '%'
        },
        {
          name: '工作满意度',
          number: '96',
          targetNumber: '100',
          warnNumber: '80',
          danwei: '%'
        },
        {
          name: '专业相关度',
          number: '87',
          targetNumber: '95',
          warnNumber: '60',
          danwei: '%'
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
    this.initResource2Chart()
    this.resource2ChartRes()
    this.initResource3Chart1()
    this.resource3ChartRes1()
    this.initResource3Chart2()
    this.resource3ChartRes2()
    this.initResource3Chart3()
    this.resource3ChartRes3()
    this.initResource3Chart4()
    this.resource3ChartRes4()
  },
  methods: {
    initResource2Chart() {
      console.log('生成资源图21')
      // var resource1Chart = document.getElementById('resource1Chart')
      var resource2Chart = this.$echarts.init(document.getElementById('resource2Chart'), 'light')
      this.resource2Chart = resource2Chart
      // var testChart1 = echarts.init(resource1Chart)
      var app = {}
      var option
      option = {
        title: {
          // text: '各课程成绩'
          // subtext: '纯属虚构'
        },
        tooltip: {
          trigger: 'axis',
          axisPointer: {
            type: 'cross',
            label: {
              backgroundColor: '#283b56'
            }
          }
        },
        legend: {
          data: ['优秀', '良好', '中等', '不及格']
        },
        toolbox: {
          show: true,
          feature: {
            dataView: { readOnly: false },
            restore: {},
            saveAsImage: {}
          }
        },
        dataZoom: {
          show: false,
          start: 0,
          end: 100
        },
        xAxis: [
          {
            type: 'category',
            boundaryGap: true,
            data: (function() {
              var now = new Date()
              var res = []
              var len = 10
              while (len--) {
                res.unshift(now.toLocaleTimeString().replace(/^\D*/, ''))
                now = new Date(now - 2000)
              }
              return res
            })()
          },
          {
            type: 'category',
            boundaryGap: true,
            data: (function() {
              var res = []
              var len = 10
              while (len--) {
                res.push(10 - len - 1)
              }
              return res
            })()
          }
        ],
        yAxis: [
          {
            type: 'value',
            scale: true,
            name: '比例',
            max: 100,
            min: 0,
            boundaryGap: [0.2, 0.2]
          },
          {
            type: 'value',
            scale: true,
            name: '预购量',
            max: 1200,
            min: 0,
            show: false,
            boundaryGap: [0.2, 0.2]
          }
        ],
        series: [
          {
            name: '优秀',
            type: 'bar',
            xAxisIndex: 1,
            yAxisIndex: 1,
            itemStyle: {
              color: '#4372e7'
            },
            data: (function() {
              var res = []
              var len = 10
              while (len--) {
                res.push(Math.round(Math.random() * 1000))
              }
              return res
            })()
          },
          {
            name: '良好',
            type: 'bar',
            xAxisIndex: 1,
            yAxisIndex: 1,
            itemStyle: {
              color: '#56ee15'
            },
            data: (function() {
              var res = []
              var len = 10
              while (len--) {
                res.push(Math.round(Math.random() * 1000))
              }
              return res
            })()
          },
          {
            name: '中等',
            type: 'bar',
            xAxisIndex: 1,
            yAxisIndex: 1,
            itemStyle: {
              color: '#fac858'
            },
            data: (function() {
              var res = []
              var len = 10
              while (len--) {
                res.push(Math.round(Math.random() * 1000))
              }
              return res
            })()
          },
          {
            name: '不及格',
            type: 'bar',
            xAxisIndex: 1,
            yAxisIndex: 1,
            itemStyle: {
              color: '#ee6666'
            },
            data: (function() {
              var res = []
              var len = 10
              while (len--) {
                res.push(Math.round(Math.random() * 1000))
              }
              return res
            })()
          }
        ]
      }

      app.count = 11
      setInterval(function() {
        var axisData = (new Date()).toLocaleTimeString().replace(/^\D*/, '')
        var data0 = option.series[0].data
        var data1 = option.series[1].data
        data0.shift()
        data0.push(Math.round(Math.random() * 1000))
        data1.shift()
        data1.push((Math.random() * 10 + 5).toFixed(1) - 0)

        option.xAxis[0].data.shift()
        option.xAxis[0].data.push(axisData)
        option.xAxis[1].data.shift()
        option.xAxis[1].data.push(app.count++)

        resource2Chart.setOption(option)
      }, 3000)
      option && resource2Chart.setOption(option)
    },
    resource2ChartRes() {
      console.log('资源图21变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource2Chart').offsetWidth
        const h = document.getElementById('resource2Chart').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource2Chart.resize(resize)
        }, 100)
      })
    },
    initResource3Chart1() {
      console.log('生成资源图31')
      // var resource1Chart = document.getElementById('resource1Chart')
      var resource3Chart1 = this.$echarts.init(document.getElementById('resource3Chart1'), 'light')
      this.resource3Chart1 = resource3Chart1
      // var testChart1 = echarts.init(resource1Chart)
      var optionArray = [{
        title: {
          text: '成绩分布',
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
            name: '成绩分布',
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
              { value: 1048, name: '优秀' },
              { value: 735, name: '良好' },
              { value: 735, name: '中等' },
              { value: 580, name: '不及格' }
            ]
          }
        ]
      },
      {
        title: {
          text: '成绩分布',
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
            name: '成绩分布',
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
              { value: 758, name: '优秀' },
              { value: 425, name: '良好' },
              { value: 935, name: '中等' },
              { value: 650, name: '不及格' }
            ]
          }
        ]
      },
      {
        title: {
          text: '成绩分布',
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
            name: '成绩分布',
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
              { value: 548, name: '优秀' },
              { value: 256, name: '良好' },
              { value: 635, name: '中等' },
              { value: 380, name: '不及格' }
            ]
          }
        ]
      }]
      this.resource3Chart1.setOption(optionArray[0])
      // setTimeout(() => {
      //   this.testBingChart.setOption(option2)
      // }, 2000)
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource3Chart1.setOption(optionArray[i])
      }, 3000)
    },
    resource3ChartRes1() {
      console.log('资源图31变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource3Chart1').offsetWidth
        const h = document.getElementById('resource3Chart1').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource3Chart1.resize(resize)
        }, 100)
      })
    },
    initResource3Chart2() {
      console.log('生成资源图32')
      // var resource1Chart = document.getElementById('resource1Chart')
      var resource3Chart2 = this.$echarts.init(document.getElementById('resource3Chart2'), 'light')
      this.resource3Chart2 = resource3Chart2
      // var testChart1 = echarts.init(resource1Chart)
      var optionArray = [{
        title: {
          text: '缓补考情况',
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
            name: '缓补考情况',
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
              { value: 1048, name: '清考' },
              { value: 735, name: '补考' },
              { value: 580, name: '缓考' }
            ]
          }
        ]
      },
      {
        title: {
          text: '缓补考情况',
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
            name: '缓补考情况',
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
              { value: 568, name: '清考' },
              { value: 205, name: '补考' },
              { value: 70, name: '缓考' }
            ]
          }
        ]
      },
      {
        title: {
          text: '缓补考情况',
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
            name: '缓补考情况',
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
              { value: 148, name: '清考' },
              { value: 35, name: '补考' },
              { value: 80, name: '缓考' }
            ]
          }
        ]
      }]
      this.resource3Chart2.setOption(optionArray[0])
      // setTimeout(() => {
      //   this.testBingChart.setOption(option2)
      // }, 2000)
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource3Chart2.setOption(optionArray[i])
      }, 3000)
    },
    resource3ChartRes2() {
      console.log('资源图32变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource3Chart2').offsetWidth
        const h = document.getElementById('resource3Chart2').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource3Chart2.resize(resize)
        }, 100)
      })
    },
    initResource3Chart3() {
      console.log('生成资源图33')
      // var resource1Chart = document.getElementById('resource1Chart')
      var resource3Chart3 = this.$echarts.init(document.getElementById('resource3Chart3'), 'light')
      this.resource3Chart3 = resource3Chart3
      // var testChart1 = echarts.init(resource1Chart)
      var optionArray = [{
        title: {
          text: '英语等级过级率',
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
            name: '英语等级过级率',
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
              { value: 1048, name: '英语四级' },
              { value: 735, name: '英语六级' }
            ]
          }
        ]
      },
      {
        title: {
          text: '英语等级过级率',
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
            name: '英语等级过级率',
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
              { value: 560, name: '英语四级' },
              { value: 360, name: '英语六级' }
            ]
          }
        ]
      },
      {
        title: {
          text: '英语等级过级率',
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
            name: '英语等级过级率',
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
              { value: 360, name: '英语四级' },
              { value: 256, name: '英语六级' }
            ]
          }
        ]
      }]
      this.resource3Chart3.setOption(optionArray[0])
      // setTimeout(() => {
      //   this.testBingChart.setOption(option2)
      // }, 2000)
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource3Chart3.setOption(optionArray[i])
      }, 3000)
    },
    resource3ChartRes3() {
      console.log('资源图33变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource3Chart3').offsetWidth
        const h = document.getElementById('resource3Chart3').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource3Chart3.resize(resize)
        }, 100)
      })
    },
    initResource3Chart4() {
      console.log('生成资源图34')
      // var resource1Chart = document.getElementById('resource1Chart')
      var resource3Chart4 = this.$echarts.init(document.getElementById('resource3Chart4'), 'light')
      this.resource3Chart4 = resource3Chart4
      // var testChart1 = echarts.init(resource1Chart)
      var optionArray = [{
        title: {
          text: '计算机等级过级率',
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
            name: '计算机等级过级率',
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
              { value: 1048, name: '计算机一级' },
              { value: 735, name: '计算机二级' },
              { value: 735, name: '计算机三级' }
            ]
          }
        ]
      },
      {
        title: {
          text: '计算机等级过级率',
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
            name: '计算机等级过级率',
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
              { value: 1000, name: '计算机一级' },
              { value: 700, name: '计算机二级' },
              { value: 300, name: '计算机三级' }
            ]
          }
        ]
      },
      {
        title: {
          text: '计算机等级过级率',
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
            name: '计算机等级过级率',
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
              { value: 962, name: '计算机一级' },
              { value: 680, name: '计算机二级' },
              { value: 450, name: '计算机三级' }
            ]
          }
        ]
      }]
      this.resource3Chart4.setOption(optionArray[0])
      // setTimeout(() => {
      //   this.testBingChart.setOption(option2)
      // }, 2000)
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource3Chart4.setOption(optionArray[i])
      }, 3000)
    },
    resource3ChartRes4() {
      console.log('资源图34变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource3Chart4').offsetWidth
        const h = document.getElementById('resource3Chart4').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource3Chart4.resize(resize)
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
.container1 {
  float: left;
  width: 33%;
  height: 88%;
  /*background-color: #cb29f8;*/
}
.container2 {
  float: left;
  width: 47%;
  height: 88%;
  /*background-color: #7bace7;*/
}
.container3 {
  float: left;
  width: 20%;
  height: 88%;
  /*background-color: #85e580;*/
}
.cure_container {
  /*display: inline-block;*/
  float: left;
  width: 100%;
  height: 100%;
  /*background-color: skyblue;*/
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

/*.cure_container {*/
/*  !*display: inline-block;*!*/
/*  float: left;*/
/*  width: 33%;*/
/*  height: 100%;*/
/*  !*background-color: skyblue;*!*/
/*}*/
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
.resource1_container {
  float: left;
  width: 100%;
  height: 100%;
  /*display: inline-block;*/
  /*background-color: #129ad2;*/
}
.resource1_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.resource1_title span {
  font-size: 1rem;
  display: inline-block;
  margin-left: 0.5rem;
  color: #6b7179;
}
.triangle-right-one {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #e3126d;
  border-bottom: 0.5rem solid transparent;
}
.resource1_chart_container {
  width: 100%;
  height: 88%;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  /*background-color: #6dc483;*/
}
.show_card_container {
  width: 45%;
  height: 28%;
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
  width: 60%;
  height: 60%;
  margin-top: 20%;
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
}
.number_container {
  text-align: center;
  margin-top: -5%;
}
.number_container span {
  font-size: 1.8rem;
  font-weight: bold;
  color: #4dbae7;
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
.triangle-right-three {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #8000ff;
  border-bottom: 0.5rem solid transparent;
}
.container21 {
  float: left;
  width: 100%;
  height: 7%;
  /*display: inline-block;*/
  /*background-color: #6dc483;*/
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
.triangle-right-two {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #147ae7;
  border-bottom: 0.5rem solid transparent;
}
.container22 {
  float: left;
  width: 100%;
  height: 35%;
  /*display: inline-block;*/
  /*background-color: #32e05e;*/
}
.container23 {
  float: left;
  width: 100%;
  height: 60%;
  /*display: inline-block;*/
  /*background-color: #52b86c;*/
}
.container23_layer1 {
  float: left;
  width: 100%;
  height: 50%;
  display: inline-block;
  /*background-color: #48c2cd;*/
}
.container23_layer2 {
  float: left;
  width: 100%;
  height: 50%;
  /*display: inline-block;*/
  /*background-color: #389fe3;*/
}
.stuChartOne {
  float: left;
  width: 50%;
  height: 100%;
  /*margin-left: 5%;*/
  display: inline-block;
  /*background-color: #52e947;*/
}
.containerChart1 {
  float: right;
  width: 70%;
  height: 100%;
  /*margin-right: 5%;*/
  /*background-color: #85e363;*/
}
.containerChart2 {
  /*float: left;*/
  width: 70%;
  height: 100%;
  /*margin-right: 5%;*/
  /*background-color: #5cd75e;*/
}
.stuChartTwo {
  float: left;
  width: 50%;
  height: 100%;
  display: inline-block;
  /*background-color: #714bd7;*/
}
.show_card_container_two {
  width: 70%;
  height: 8%;
  margin-left: 10%;
  margin-bottom: 1%;
  border-radius: 1rem;
  background: white;
  box-shadow: 0.2rem 0.2rem 0.1rem #cecdcd;
}
.left_icon_container_two {
  float: left;
  height: 100%;
  width: 30%;
  /*background: green;*/
  background: deepskyblue;
  border-radius: 1rem 0 0 1rem;
  text-align: center;
}
.left_icon_container_two img {
  width: 60%;
  height: 60%;
  margin-top: 20%;
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
  margin-top: 10%;
}
.text_header_two span {
  color: #48494b;
  font-weight: bold;
}
.number_container_two {
  text-align: center;
  margin-top: -5%;
}
.number_container_two span {
  font-size: 1.8rem;
  font-weight: bold;
  color: #4dbae7;
}
</style>

