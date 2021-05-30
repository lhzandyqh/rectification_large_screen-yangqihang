<template>
  <div class="all_container">
    <Header style="width: 100%;height: 12%" />
    <div style="width: 100%;height: 44%;">
      <div class="cure_container">
        <div class="cure_title">
          <div class="triangle-right" />
          <span>专业基本情况数据展示</span>
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
          <span>专业总览</span>
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
        <div class="resource2_title">
          <div class="triangle-right-three" />
          <span>专业教学资源</span>
        </div>
        <div class="resource2_chart_container">
          <div class="resource2Chart" style="margin-top: 15%">
            <div class="echart_container">
              <div id="resource2Chart" style="height: 100%;width: 100%" />
            </div>
          </div>
        </div>
      </div>
      <div class="resource3_container">
        <div class="resource3_title">
          <div class="triangle-right-four" />
          <span>招生情况</span>
        </div>
        <div class="resource3_chart_container">
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/shengnei.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>省内生源数量</span>
              </div>
              <div class="number_container">
                <span>56492</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/shengwai.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>省外生源数量</span>
              </div>
              <div class="number_container">
                <span>2349</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/jihua.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>计划招生人数</span>
              </div>
              <div class="number_container">
                <span>43020</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/shiji.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>实际录取人数</span>
              </div>
              <div class="number_container">
                <span>41039</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/diyi.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>第一志愿报到率</span>
              </div>
              <div class="number_container">
                <span>93%</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/zong.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>总报到率</span>
              </div>
              <div class="number_container">
                <span>95%</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="resource4_container">
        <div class="resource4_title">
          <div class="triangle-right-five" />
          <span>专业培养情况</span>
        </div>
        <div class="resource4_chart_container">
          <div class="resource4ChartOne">
            <div class="echart_container">
              <div id="resource4Chart" style="height: 100%;width: 100%;" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/views/myComponents/head/proheader'
import vueSeamlessScroll from 'vue-seamless-scroll'
// import * as echarts from 'echarts'
export default {
  name: 'MajorIndex',
  components: {
    Header,
    vueSeamlessScroll
  },
  data() {
    return {
      CardPartsStatisticsList: [
        {
          name: '专业总数',
          number: '30',
          targetNumber: '45',
          warnNumber: '20',
          danwei: '个'
        },
        {
          name: '国家示范专业数',
          number: '15',
          targetNumber: '25',
          warnNumber: '5',
          danwei: '个'
        },
        {
          name: '骨干专业数',
          number: '19',
          targetNumber: '26',
          warnNumber: '15',
          danwei: '个'
        },
        {
          name: '一流专业数',
          number: '10',
          targetNumber: '20',
          warnNumber: '15',
          danwei: '个'
        },
        {
          name: '重点专业数',
          number: '16',
          targetNumber: '27',
          warnNumber: '10',
          danwei: '个'
        },
        {
          name: '专业综合改革试点数',
          number: '12',
          targetNumber: '19',
          warnNumber: '10',
          danwei: '个'
        },
        {
          name: '专业教学资源库数量',
          number: '76',
          targetNumber: '200',
          warnNumber: '30',
          danwei: '个'
        },
        {
          name: '精品在线开放课程数量',
          number: '12',
          targetNumber: '40',
          warnNumber: '10',
          danwei: '个'
        },
        {
          name: '实训基地数量',
          number: '8',
          targetNumber: '10',
          warnNumber: '5',
          danwei: '个'
        },
        {
          name: '生均仪器设备值',
          number: '6',
          targetNumber: '10',
          warnNumber: '3',
          danwei: '个'
        },
        {
          name: '就业率',
          number: '96',
          targetNumber: '100',
          warnNumber: '70',
          danwei: '%'
        },
        {
          name: '正常招生专业数',
          number: '33',
          targetNumber: '36',
          warnNumber: '20',
          danwei: '个'
        },
        {
          name: '新增专业数',
          number: '2',
          targetNumber: '5',
          warnNumber: '4',
          danwei: '个'
        },
        {
          name: '停招专业数',
          number: '1',
          targetNumber: '0',
          warnNumber: '3',
          danwei: '个'
        },
        {
          name: '撤销专业数',
          number: '0',
          targetNumber: '0',
          warnNumber: '5',
          danwei: '个'
        },
        {
          name: '3年在校人数总和数',
          number: '22463',
          targetNumber: '26000',
          warnNumber: '19600',
          danwei: '人'
        },
        {
          name: '毕业生人数',
          number: '22112',
          targetNumber: '22463',
          warnNumber: '21000',
          danwei: '人'
        },
        {
          name: '毕业率',
          number: '96',
          targetNumber: '99',
          warnNumber: '90',
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
    this.initResource1()
    this.resourceRes1()
    this.initResource2()
    this.resourceRes2()
    this.initResource4()
    this.resourceRes4()
  },
  methods: {
    initResource1() {
      console.log('生成资源图1')
      var app = {}
      // var resource1Chart = document.getElementById('resource1Chart')
      var resource1Chart = this.$echarts.init(document.getElementById('resource1Chart'), 'light')
      this.resource1Chart = resource1Chart
      // var testChart1 = echarts.init(resource1Chart)
      var option
      option = {
        title: {
          text: '动态数据',
          subtext: '纯属虚构'
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
          data: ['专业教学资源库数量', '精品在线开放课程数量', '专业教学总课时量', '师资']
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
            name: '人',
            max: 100,
            min: 0,
            boundaryGap: [0.2, 0.2]
          },
          {
            type: 'value',
            scale: true,
            name: '个',
            max: 1200,
            min: 0,
            boundaryGap: [0.2, 0.2]
          }
        ],
        series: [
          {
            name: '专业教学资源库数量',
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
            name: '精品在线开放课程数量',
            type: 'bar',
            xAxisIndex: 1,
            yAxisIndex: 1,
            itemStyle: {
              color: '#6edd62'
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
            name: '专业教学总课时量',
            type: 'bar',
            xAxisIndex: 1,
            yAxisIndex: 1,
            itemStyle: {
              color: '#e344b6'
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
            name: '师资',
            type: 'line',
            itemStyle: {
              color: '#e21111'
            },
            data: (function() {
              var res = []
              var len = 0
              while (len < 10) {
                res.push((Math.random() * 10 + 5).toFixed(1) - 0)
                len++
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

        resource1Chart.setOption(option)
      }, 2100)

      option && resource1Chart.setOption(option)
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
    initResource2() {
      console.log('生成专业资源图')
      this.resource2Chart = this.$echarts.init(document.getElementById('resource2Chart'), 'light')
      var optionArray = [{
        title: {
          text: '临床医学',
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
            name: '临床医学',
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
              { value: 1048, name: '专业教学资源库数量' },
              { value: 735, name: '精品在线开放课程数量' },
              { value: 580, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '口腔医学',
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
            name: '口腔医学',
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
              { value: 1002, name: '专业教学资源库数量' },
              { value: 156, name: '精品在线开放课程数量' },
              { value: 654, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '护理学',
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
            name: '护理学',
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
              { value: 865, name: '专业教学资源库数量' },
              { value: 752, name: '精品在线开放课程数量' },
              { value: 693, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '助产',
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
            name: '助产',
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
              { value: 236, name: '专业教学资源库数量' },
              { value: 654, name: '精品在线开放课程数量' },
              { value: 854, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '药学',
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
            name: '药学',
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
              { value: 658, name: '专业教学资源库数量' },
              { value: 258, name: '精品在线开放课程数量' },
              { value: 580, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '卫生信息管理',
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
            name: '卫生信息管理',
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
              { value: 448, name: '专业教学资源库数量' },
              { value: 1035, name: '精品在线开放课程数量' },
              { value: 360, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '医学检验技术',
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
            name: '医学检验技术',
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
              { value: 635, name: '专业教学资源库数量' },
              { value: 785, name: '精品在线开放课程数量' },
              { value: 580, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '中医学',
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
            name: '中医学',
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
              { value: 635, name: '专业教学资源库数量' },
              { value: 598, name: '精品在线开放课程数量' },
              { value: 758, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '医学影像技术',
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
            name: '医学影像技术',
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
              { value: 948, name: '专业教学资源库数量' },
              { value: 335, name: '精品在线开放课程数量' },
              { value: 680, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '康复医疗技术',
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
            name: '康复医疗技术',
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
              { value: 369, name: '专业教学资源库数量' },
              { value: 654, name: '精品在线开放课程数量' },
              { value: 580, name: '教材概况' }
            ]
          }
        ]
      }, {
        title: {
          text: '医学美容技术',
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
            name: '医疗美容技术',
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
              { value: 364, name: '专业教学资源库数量' },
              { value: 952, name: '精品在线开放课程数量' },
              { value: 587, name: '教材概况' }
            ]
          }
        ]
      }]
      this.resource2Chart.setOption(optionArray[0])
      // setTimeout(() => {
      //   this.testBingChart.setOption(option2)
      // }, 2000)
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource2Chart.setOption(optionArray[i])
      }, 1000)
    },
    resourceRes2() {
      console.log('专业资源图变形')
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
    initResource4() {
      console.log('生成专业资源图4')
      var resource4Chart = this.$echarts.init(document.getElementById('resource4Chart'), 'light')
      // this.testChart = this.$echarts.init(document.getElementById('testChart'), 'light')
      this.resource4Chart = resource4Chart
      var optionArray = [
        {
          title: {
            text: '   校企合作图'
          },
          legend: [
            {
              x: 'center',
              data: ['现代学徒制培养人数', '订单班培养人数', '合作企业接收顶岗实习学生人数', '捐赠设备总值']
            },
            {
              x: 'center',
              top: '5%',
              data: ['合作企业数量', '联合开发课程数量', '联合开发教材数量']
            }
          ],
          tooltip: {
            trigger: 'axis',
            showContent: false
          },
          dataset: {
            source: [
              ['major', '临床医学', '口腔医学', '护理学', '助产', '药学', '卫生信息管理', '医学检验技术', '中医学',
                '医学影像技术', '康复治疗技术', '医学美容技术'],
              ['现代学徒制培养人数', 100, 200, 102, 39, 100, 85, 86, 165, 98, 76, 123],
              ['订单班培养人数', 100, 56, 205, 35, 87, 96, 78, 65, 75, 100, 100],
              ['合作企业接收顶岗实习学生人数', 100, 100, 100, 100, 100, 100, 100, 100, 100, 100, 100]
            ]
          },
          xAxis: {
            type: 'category',
            data: ['临床医学', '口腔医学', '护理学', '助产', '药学', '卫生信息管理', '医学检验技术', '中医学',
              '医学影像技术', '康复治疗技术', '医学美容技术']
          },
          yAxis: [
          // { gridIndex: 0 },
            {
              type: 'value',
              scale: true,
              name: '台',
              max: 500,
              min: 0,
              boundaryGap: [0.2, 0.2]
            }, {
              type: 'value',
              scale: true,
              name: '课程数',
              max: 500,
              min: 0,
              boundaryGap: [0.2, 0.2]
            }],
          grid: { top: '55%' },
          series: [
            { name: '捐赠设备总值',
              type: 'line',
              // smooth: true,
              itemStyle: {
                color: '#ee6666'
              },
              seriesLayoutBy: 'row',
              data: [120, 132, 101, 134, 90, 230, 210, 120, 230, 90, 80],
              emphasis: { focus: 'series' }},
            // { name: '联合开发课程数量',
            //   type: 'bar',
            //   seriesLayoutBy: 'row',
            //   itemStyle: {
            //     color: '#91cc75'
            //   },
            //   xAxis: { type: 'category' },
            //   yAxis: {},
            //   dataset: {
            //     source: [
            //       ['product', '联合开发课程数量', '合作企业数量', '联合开发教材数量'],
            //       ['临床医学', 43, 85, 20],
            //       ['口腔医学', 43, 85, 20],
            //       ['护理学', 43, 85, 20],
            //       ['助产', 43, 85, 20],
            //       ['药学', 43, 85, 20],
            //       ['卫生信息管理', 43, 85, 20],
            //       ['医学检验技术', 43, 85, 20],
            //       ['中医学', 43, 85, 20],
            //       ['医学影像技术', 43, 85, 20],
            //       ['康复治疗技术', 43, 85, 20],
            //       ['医学美容技术', 43, 85, 20]
            //     ]
            //   },
            //   emphasis: { focus: 'series' }
            // },
            { name: '合作企业数量',
              type: 'bar',
              seriesLayoutBy: 'row',
              itemStyle: {
                color: '#5470c6'
              },
              data: [120, 132, 101, 134, 90, 230, 210, 120, 230, 90, 80],
              // [120, 132, 101, 134, 90, 230, 210, 120, 230, 90, 80],
              // [120, 132, 101, 134, 90, 230, 210, 120, 230, 90, 80],
              emphasis: { focus: 'series' }},
            // { type: 'line', smooth: true, seriesLayoutBy: 'row', emphasis: { focus: 'series' }},
            // { type: 'line', smooth: true, seriesLayoutBy: 'row', emphasis: { focus: 'series' }},
            { name: '联合开发课程数量',
              type: 'bar',
              seriesLayoutBy: 'row',
              itemStyle: {
                color: '#91cc75'
              },
              data: [120, 132, 101, 134, 90, 230, 210, 120, 230, 90, 80],
              emphasis: { focus: 'series' }},
            { name: '联合开发教材数量',
              type: 'bar',
              seriesLayoutBy: 'row',
              itemStyle: {
                color: '#ee6666'
              },
              data: [120, 132, 101, 134, 90, 230, 210, 120, 230, 90, 80],
              emphasis: { focus: 'series' }},
            {
              type: 'pie',
              id: 'pie',
              top: '6%',
              radius: '30%',
              center: ['50%', '25%'],
              emphasis: { focus: 'data' },
              label: {
                formatter: '{b}: {@临床医学} ({d}%)'
              },
              encode: {
                itemName: 'major',
                value: '临床医学',
                tooltip: '临床医学'
              }
            }
          ]
        },
        {
          title: {
            text: '   培养效果图'
          },
          tooltip: {
            trigger: 'axis'
          },
          legend: {
            data: ['考试通过率', '毕业率', '就业率', '优秀率', '及格率', '不及格率']
          },
          grid: {
            left: '3%',
            right: '4%',
            bottom: '3%',
            containLabel: true
          },
          toolbox: {
            feature: {
              saveAsImage: {}
            }
          },
          xAxis: {
            type: 'category',
            boundaryGap: false,
            data: ['临床医学', '口腔医学', '护理学', '助产', '药学', '卫生信息管理', '医学检验技术', '中医学',
              '医学影像技术', '康复治疗技术', '医学美容技术']
          },
          yAxis: {
            type: 'value',
            scale: true,
            name: '比例',
            max: 100,
            min: 0,
            boundaryGap: [0.2, 0.2]
          },
          series: [
            {
              name: '考试通过率',
              type: 'line',
              stack: '总量',
              data: [20, 32, 11, 14, 20, 23, 21, 12, 12, 21, 14]
            },
            {
              name: '毕业率',
              type: 'line',
              stack: '总量',
              data: [22, 12, 19, 24, 29, 33, 31, 22, 12, 11, 34]
            },
            {
              name: '就业率',
              type: 'line',
              stack: '总量',
              data: [15, 23, 21, 54, 10, 30, 40, 50, 23, 54, 19]
            },
            {
              name: '优秀率',
              type: 'line',
              stack: '总量',
              data: [32, 32, 31, 34, 30, 30, 32, 20, 31, 14, 90]
            },
            {
              name: '及格率',
              type: 'line',
              stack: '总量',
              data: [12, 19, 31, 94, 20, 30, 12, 92, 51, 44, 60]
            },
            {
              name: '不及格率',
              type: 'line',
              stack: '总量',
              data: [56, 32, 91, 34, 12, 30, 32, 82, 52, 34, 29]
            }
          ]
        },
        {
          title: {
            text: '   顶岗实习图'
          },
          legend: {},
          tooltip: {},
          dataset: {
            source: [
              ['product', '顶岗实习学生人数', '顶岗实习录用学生数'],
              ['临床医学', 43, 85],
              ['口腔医学', 43, 85],
              ['护理学', 43, 85],
              ['助产', 43, 85],
              ['药学', 43, 85],
              ['卫生信息管理', 43, 85],
              ['医学检验技术', 43, 85],
              ['中医学', 43, 85],
              ['医学影像技术', 43, 85],
              ['康复治疗技术', 43, 85],
              ['医学美容技术', 43, 85]
            ]
          },
          xAxis: { type: 'category' },
          yAxis: {},
          series: [
            { type: 'bar' },
            { type: 'bar' }
          ]
        }
        // {
        //   title: {
        //     text: '   顶岗实习图2'
        //   },
        //   legend: {},
        //   tooltip: {},
        //   dataset: {
        //     source: [
        //       ['product', '顶岗实习学生人数', '顶岗实习录用学生数', '测试'],
        //       ['临床医学', 100, 100, 12],
        //       ['口腔医学', 43, 85, 12],
        //       ['护理学', 43, 85, 12],
        //       ['助产', 43, 85, 12],
        //       ['药学', 43, 85, 12],
        //       ['卫生信息管理', 43, 85, 12],
        //       ['医学检验技术', 43, 85, 12],
        //       ['中医学', 43, 85, 12],
        //       ['医学影像技术', 43, 85, 12],
        //       ['康复治疗技术', 43, 85, 12],
        //       ['医学美容技术', 43, 85, 12]
        //     ]
        //   },
        //   xAxis: { type: 'category' },
        //   yAxis: {},
        //   series: [
        //     { type: 'bar' },
        //     { type: 'bar' }
        //   ]
        // }
      ]
      resource4Chart.on('updateAxisPointer', function(event) {
        var xAxisInfo = event.axesInfo[0]
        if (xAxisInfo) {
          var dimension = xAxisInfo.value + 1
          resource4Chart.setOption({
            series: {
              id: 'pie',
              label: {
                formatter: '{b}: {@[' + dimension + ']} ({d}%)'
              },
              encode: {
                value: dimension,
                tooltip: dimension
              }
            }
          })
        }
      })

      this.resource4Chart.setOption(optionArray[0])

      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        // this.resource4Chart.clean()
        // var resource4Chart = this.$echarts.init(document.getElementById('resource4Chart'), 'light')
        // // this.testChart = this.$echarts.init(document.getElementById('testChart'), 'light')
        // this.resource4Chart = resource4Chart
        var nowOption = {}
        nowOption = optionArray[i]
        this.resource4Chart.setOption(nowOption, true)
      }, 1000)
    },
    resourceRes4() {
      console.log('专业资源图变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource4Chart').offsetWidth
        const h = document.getElementById('resource4Chart').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource4Chart.resize(resize)
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
  width: 50%;
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
  width: 17%;
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
  border-left: 0.8rem solid #e2cd1d;
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
  width: 30%;
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
  border-left: 0.8rem solid #e2cd1d;
  border-bottom: 0.5rem solid transparent;
}
.resource3_chart_container {
  width: 100%;
  height: 88%;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
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
  border-left: 0.8rem solid #e21d5b;
  border-bottom: 0.5rem solid transparent;
}
.resource4_chart_container {
  width: 100%;
  height: 88%;
  /*background: #8c939d;*/
}
.resource4ChartOne {
  width: 100%;
  height: 100%;
}
.resource4_container {
  float: left;
  width: 70%;
  height: 100%;
  /*background-color: #22b0ea;*/
}

.show_card_container_two {
  width: 45%;
  height: 28%;
  border-radius: 1rem;
  background: white;
  box-shadow: 0.2rem 0.2rem 0.1rem #cecdcd;
}
.left_icon_container_two {
  float: left;
  height: 100%;
  width: 40%;
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
