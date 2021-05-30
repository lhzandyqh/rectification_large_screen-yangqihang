<template>
  <div class="all_container">
    <Header style="width: 100%;height: 12%" />
    <div style="width: 100%;height: 44%;">
      <div class="cure_container">
        <div class="cure_title">
          <div class="triangle-right" />
          <span>基本情况</span>
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
          <span>课程资源</span>
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
          <div class="triangle-right-two" />
          <span>课堂教学</span>
        </div>
        <div class="resource2Chart1">
          <!--          <div class="echart_container">-->
          <!--            <div id="resource2Chart" style="height: 100%;width: 100%;" />-->
          <!--          </div>-->
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/zuoye.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>作业布置次数</span>
              </div>
              <div class="number_container">
                <span>23</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/ceshi.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>随堂测试次数</span>
              </div>
              <div class="number_container">
                <span>35</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/taolun.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>小组讨论次数</span>
              </div>
              <div class="number_container">
                <span>92</span>
              </div>
            </div>
          </div>
          <div class="show_card_container">
            <div class="left_icon_container">
              <img src="../../assets/icon/dayi.png">
            </div>
            <div class="right_text_container">
              <div class="text_header">
                <span>答疑次数</span>
              </div>
              <div class="number_container">
                <span>156</span>
              </div>
            </div>
          </div>
        </div>
        <div class="resource2Chart2">
          <div class="resource2Chart3">
            <div class="echart_container">
              <div id="resource2ChartOne" style="height: 100%;width: 100%" />
            </div>
          </div>
          <div class="resource2Chart3">
            <div class="echart_container">
              <div id="resource2ChartTwo" style="height: 100%;width: 100%" />
            </div>
          </div>
        </div>
      </div>
      <div class="resource3_container">
        <div class="resource3_title">
          <div class="triangle-right-three" />
          <span>教学评价</span>
        </div>
        <div class="resource3_chart_container">
          <div class="resource3Chart">
            <div class="echart_container">
              <div id="resource3Chart" style="height: 100%;width: 100%;" />
            </div>
          </div>
        </div>
      </div>
      <div class="resource4_container">
        <div class="resource4_title">
          <!--          <div class="triangle-right-four" />-->
          <!--          <span>招生情况</span>-->
        </div>
        <div class="resource4_chart_container">
          <!--          <div class="resource4Chart">-->
          <!--            <div class="echart_container">-->
          <!--              <div id="resource4Chart" style="height: 100%;width: 100%;" />-->
          <!--            </div>-->
          <!--          </div>-->
          <div class="show_card_container_two">
            <div class="left_icon_container_two">
              <img src="../../assets/icon/dudao.png">
            </div>
            <div class="right_text_container_two">
              <div class="text_header_two">
                <span>督导评价得分</span>
              </div>
              <div class="number_container_two">
                <span>82</span>
              </div>
            </div>
          </div>
          <div class="show_card_container_two">
            <div class="left_icon_container_two">
              <img src="../../assets/icon/xueshengpj.png">
            </div>
            <div class="right_text_container_two">
              <div class="text_header_two">
                <span>学生评价分数</span>
              </div>
              <div class="number_container_two">
                <span>90</span>
              </div>
            </div>
          </div>
          <div class="show_card_container_two">
            <div class="left_icon_container_two">
              <img src="../../assets/icon/zongti.png">
            </div>
            <div class="right_text_container_two">
              <div class="text_header_two">
                <span>总评平均成绩</span>
              </div>
              <div class="number_container_two">
                <span>88</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/views/myComponents/head/couheader'
import vueSeamlessScroll from 'vue-seamless-scroll'
// import * as echarts from 'echarts'
export default {
  name: 'CourseIndex',
  components: {
    Header,
    vueSeamlessScroll
  },
  data() {
    return {
      CardPartsStatisticsList: [
        {
          name: '课程总数',
          number: '67',
          targetNumber: '100',
          warnNumber: '45',
          danwei: '个'
        },
        {
          name: '专业核心课程数量',
          number: '32',
          targetNumber: '45',
          warnNumber: '20',
          danwei: '个'
        },
        {
          name: '骨干专业数',
          number: '16',
          targetNumber: '20',
          warnNumber: '5',
          danwei: '个'
        },
        {
          name: '精品在线开放课程',
          number: '13',
          targetNumber: '19',
          warnNumber: '5',
          danwei: '个'
        },
        {
          name: '校企合作联合开发课程',
          number: '6',
          targetNumber: '15',
          warnNumber: '5',
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
          name: '精品资源共享课',
          number: '10',
          targetNumber: '20',
          warnNumber: '4',
          danwei: '个'
        },
        {
          name: '课堂活跃度',
          number: '85',
          targetNumber: '90',
          warnNumber: '70',
          danwei: '%'
        },
        // {
        //   name: '课程-课堂教学',
        //   number: '35',
        //   targetNumber: '111',
        //   warnNumber: '45',
        //   danwei: '个'
        // },
        {
          name: '平均成绩增长率',
          number: '53',
          targetNumber: '45',
          warnNumber: '15',
          danwei: '%'
        },
        {
          name: '卷面平均成绩',
          number: '78',
          targetNumber: '90',
          warnNumber: '60',
          danwei: '分'
        },
        {
          name: '卷面成绩优秀率',
          number: '13',
          targetNumber: '20',
          warnNumber: '5',
          danwei: '%'
        },
        {
          name: '教学方法多样性',
          number: '12',
          targetNumber: '30',
          warnNumber: '10',
          danwei: '种'
        },
        {
          name: '理论课课程数量',
          number: '35',
          targetNumber: '30',
          warnNumber: '40',
          danwei: '个'
        },
        {
          name: '理论课数量占比',
          number: '52',
          targetNumber: '50',
          warnNumber: '55',
          danwei: '%'
        },
        {
          name: '实践课课程数量',
          number: '37',
          targetNumber: '42',
          warnNumber: '30',
          danwei: '个'
        },
        {
          name: '实践课数量占比',
          number: '48',
          targetNumber: '55',
          warnNumber: '45',
          danwei: '%'
        },
        {
          name: '理论课+实践课课程数量',
          number: '72',
          targetNumber: '82',
          warnNumber: '90',
          danwei: '门'
        },
        {
          name: '理论课+实践课数量占比',
          number: '80',
          targetNumber: '75',
          warnNumber: '60',
          danwei: '%'
        },
        // {
        //   name: '理论课开课数量',
        //   number: '35',
        //   targetNumber: '35',
        //   warnNumber: '30',
        //   danwei: '门'
        // },
        // {
        //   name: '理论课开课数量占比',
        //   number: '97',
        //   targetNumber: '100',
        //   warnNumber: '45',
        //   danwei: '%'
        // },
        // {
        //   name: '实践课开课数量',
        //   number: '34',
        //   targetNumber: '37',
        //   warnNumber: '45',
        //   danwei: '门'
        // },
        // {
        //   name: '实践课开课数量占比',
        //   number: '96',
        //   targetNumber: '100',
        //   warnNumber: '45',
        //   danwei: '%'
        // },
        // {
        //   name: '理论课+实践课开课数量',
        //   number: '100',
        //   targetNumber: '111',
        //   warnNumber: '45',
        //   danwei: '人'
        // },
        // {
        //   name: '理论课+实践课开课数量占比',
        //   number: '100',
        //   targetNumber: '111',
        //   warnNumber: '45',
        //   danwei: '%'
        // },
        {
          name: '课程组人数（正高级）',
          number: '23',
          targetNumber: '30',
          warnNumber: '12',
          danwei: '人'
        },
        {
          name: '课程组人数（副高级）',
          number: '19',
          targetNumber: '30',
          warnNumber: '10',
          danwei: '人'
        },
        {
          name: '课程组人数（中级）',
          number: '46',
          targetNumber: '80',
          warnNumber: '45',
          danwei: '人'
        },
        {
          name: '课程组人数（初级）',
          number: '36',
          targetNumber: '50',
          warnNumber: '10',
          danwei: '人'
        },
        {
          name: '实训项目总数',
          number: '12',
          targetNumber: '20',
          warnNumber: '5',
          danwei: '个'
        },
        {
          name: '项目开出量',
          number: '28',
          targetNumber: '30',
          warnNumber: '10',
          danwei: '个'
        },
        {
          name: '项目开出率',
          number: '96',
          targetNumber: '100',
          warnNumber: '45',
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
    this.initResource21()
    this.resourceRes21()
    this.initResource22()
    this.resourceRes22()
    this.initResource3()
    this.resourceRes3()
  },
  methods: {
    initResource1() {
      console.log('生成课程资源图')
      var resource1Chart = this.$echarts.init(document.getElementById('resource1Chart'), 'light')
      this.resource1Chart = resource1Chart
      var option = {
        xAxis: {
          type: 'category',
          data: ['在线课程数量', '在线试卷数量', '在线习题集数量', '文本数量', '图片数量', '音频数量', '视频数量', '教学资料', '知识点数量']
        },
        yAxis: {
          type: 'value',
          scale: true,
          name: '个',
          max: 500,
          min: 0,
          interval: 100,
          boundaryGap: [0.2, 0.2]
        },
        series: [{
          data: [120, 150, 380, 70, 110, 130, 450, 300, 480],
          type: 'bar'
        }]
      }

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
    initResource21() {
      console.log('生成课堂教学资源图1')
      var resource2ChartOne = this.$echarts.init(document.getElementById('resource2ChartOne'), 'light')
      this.resource2ChartOne = resource2ChartOne
      var optionArray = [
        {
          series: [{
            type: 'gauge',
            startAngle: 180,
            endAngle: 0,
            min: 0,
            max: 1,
            splitNumber: 8,
            // top: '10%',
            // left: 'center',
            axisLine: {
              lineStyle: {
                width: 6,
                color: [
                  [0, '#FF6E76'],
                  [0.25, '#FDDD60'],
                  [0.5, '#58D9F9'],
                  [0.75, '#7CFFB2'],
                  [1, '#45fc03']
                ]
              }
            },
            pointer: {
              icon: 'path://M12.8,0.7l12,40.1H0.7L12.8,0.7z',
              length: '12%',
              width: 10,
              offsetCenter: [0, '-60%'],
              itemStyle: {
                color: 'auto'
              }
            },
            axisTick: {
              length: 12,
              lineStyle: {
                color: 'auto',
                width: 2
              }
            },
            splitLine: {
              length: 20,
              lineStyle: {
                color: 'auto',
                width: 5
              }
            },
            axisLabel: {
              color: '#464646',
              fontSize: 18,
              distance: -50,
              formatter: function(value) {
                if (value === 0) {
                  return '0'
                } else if (value === 0.25) {
                  return '25%'
                } else if (value === 0.50) {
                  return '50%'
                } else if (value === 0.75) {
                  return '75%'
                } else if (value === 1) {
                  return '100%'
                }
              }
            },
            title: {
              offsetCenter: [0, '-20%'],
              fontSize: 20
            },
            detail: {
              fontSize: 25,
              offsetCenter: [0, '0%'],
              valueAnimation: true,
              formatter: function(value) {
                return Math.round(value * 100) + '%'
              },
              color: 'auto'
            },
            data: [{
              value: 0.20,
              name: '作业批改率'
              // fontSize: 10
            }]
          }]
        },
        {
          series: [{
            type: 'gauge',
            startAngle: 180,
            endAngle: 0,
            min: 0,
            max: 1,
            splitNumber: 8,
            // top: '10%',
            // left: 'center',
            axisLine: {
              lineStyle: {
                width: 6,
                color: [
                  [0, '#FF6E76'],
                  [0.25, '#FDDD60'],
                  [0.5, '#58D9F9'],
                  [0.75, '#7CFFB2'],
                  [1, '#45fc03']
                ]
              }
            },
            pointer: {
              icon: 'path://M12.8,0.7l12,40.1H0.7L12.8,0.7z',
              length: '12%',
              width: 10,
              offsetCenter: [0, '-60%'],
              itemStyle: {
                color: 'auto'
              }
            },
            axisTick: {
              length: 12,
              lineStyle: {
                color: 'auto',
                width: 2
              }
            },
            splitLine: {
              length: 20,
              lineStyle: {
                color: 'auto',
                width: 5
              }
            },
            axisLabel: {
              color: '#464646',
              fontSize: 18,
              distance: -50,
              formatter: function(value) {
                if (value === 0) {
                  return '0'
                } else if (value === 0.25) {
                  return '25%'
                } else if (value === 0.50) {
                  return '50%'
                } else if (value === 0.75) {
                  return '75%'
                } else if (value === 1) {
                  return '100%'
                }
              }
            },
            title: {
              offsetCenter: [0, '-20%'],
              fontSize: 20
            },
            detail: {
              fontSize: 25,
              offsetCenter: [0, '0%'],
              valueAnimation: true,
              formatter: function(value) {
                return Math.round(value * 100) + '%'
              },
              color: 'auto'
            },
            data: [{
              value: 0.50,
              name: '学生签到率'
              // fontSize: 10
            }]
          }]
        }
      ]

      this.resource2ChartOne.setOption(optionArray[0])
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource2ChartOne.setOption(optionArray[i])
      }, 1000)
    },
    resourceRes21() {
      console.log('资源图1变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource2ChartOne').offsetWidth
        const h = document.getElementById('resource2ChartOne').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource2ChartOne.resize(resize)
        }, 100)
      })
    },
    initResource22() {
      console.log('生成课堂教学资源图2')
      var resource2ChartTwo = this.$echarts.init(document.getElementById('resource2ChartTwo'), 'light')
      this.resource2ChartTwo = resource2ChartTwo
      var optionArray = [
        {
          series: [{
            type: 'gauge',
            startAngle: 180,
            endAngle: 0,
            min: 0,
            max: 1,
            splitNumber: 8,
            // top: '10%',
            // left: 'center',
            axisLine: {
              lineStyle: {
                width: 6,
                color: [
                  [0, '#FF6E76'],
                  [0.25, '#FDDD60'],
                  [0.5, '#58D9F9'],
                  [0.75, '#7CFFB2'],
                  [1, '#45fc03']
                ]
              }
            },
            pointer: {
              icon: 'path://M12.8,0.7l12,40.1H0.7L12.8,0.7z',
              length: '12%',
              width: 10,
              offsetCenter: [0, '-60%'],
              itemStyle: {
                color: 'auto'
              }
            },
            axisTick: {
              length: 12,
              lineStyle: {
                color: 'auto',
                width: 2
              }
            },
            splitLine: {
              length: 20,
              lineStyle: {
                color: 'auto',
                width: 5
              }
            },
            axisLabel: {
              color: '#464646',
              fontSize: 18,
              distance: -50,
              formatter: function(value) {
                if (value === 0) {
                  return '0'
                } else if (value === 0.25) {
                  return '25%'
                } else if (value === 0.50) {
                  return '50%'
                } else if (value === 0.75) {
                  return '75%'
                } else if (value === 1) {
                  return '100%'
                }
              }
            },
            title: {
              offsetCenter: [0, '-20%'],
              fontSize: 20
            },
            detail: {
              fontSize: 25,
              offsetCenter: [0, '0%'],
              valueAnimation: true,
              formatter: function(value) {
                return Math.round(value * 100) + '%'
              },
              color: 'auto'
            },
            data: [{
              value: 0.60,
              name: '学生提问率'
              // fontSize: 10
            }]
          }]
        },
        {
          series: [{
            type: 'gauge',
            startAngle: 180,
            endAngle: 0,
            min: 0,
            max: 1,
            splitNumber: 8,
            // top: '10%',
            // left: 'center',
            axisLine: {
              lineStyle: {
                width: 6,
                color: [
                  [0, '#FF6E76'],
                  [0.25, '#FDDD60'],
                  [0.5, '#58D9F9'],
                  [0.75, '#7CFFB2'],
                  [1, '#45fc03']
                ]
              }
            },
            pointer: {
              icon: 'path://M12.8,0.7l12,40.1H0.7L12.8,0.7z',
              length: '12%',
              width: 10,
              offsetCenter: [0, '-60%'],
              itemStyle: {
                color: 'auto'
              }
            },
            axisTick: {
              length: 12,
              lineStyle: {
                color: 'auto',
                width: 2
              }
            },
            splitLine: {
              length: 20,
              lineStyle: {
                color: 'auto',
                width: 5
              }
            },
            axisLabel: {
              color: '#464646',
              fontSize: 18,
              distance: -50,
              formatter: function(value) {
                if (value === 0) {
                  return '0'
                } else if (value === 0.25) {
                  return '25%'
                } else if (value === 0.50) {
                  return '50%'
                } else if (value === 0.75) {
                  return '75%'
                } else if (value === 1) {
                  return '100%'
                }
              }
            },
            title: {
              offsetCenter: [0, '-20%'],
              fontSize: 20
            },
            detail: {
              fontSize: 25,
              offsetCenter: [0, '0%'],
              valueAnimation: true,
              formatter: function(value) {
                return Math.round(value * 100) + '%'
              },
              color: 'auto'
            },
            data: [{
              value: 0.90,
              name: '论坛发帖率'
              // fontSize: 10
            }]
          }]
        }
      ]

      this.resource2ChartTwo.setOption(optionArray[0])
      var i = 0
      setInterval(() => {
        i = i + 1
        if (i > optionArray.length) {
          i = 0
        }
        this.resource2ChartTwo.setOption(optionArray[i])
      }, 1000)
    },
    resourceRes22() {
      console.log('课堂教学资源图2变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource2ChartTwo').offsetWidth
        const h = document.getElementById('resource2ChartTwo').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource2ChartTwo.resize(resize)
        }, 100)
      })
    },
    initResource3() {
      console.log('生成教学评价资源图')
      var resource3Chart = this.$echarts.init(document.getElementById('resource3Chart'), 'light')
      this.resource3Chart = resource3Chart
      var option = {
        xAxis: {
          type: 'category',
          data: ['调课占比', '代课占比', '课堂满意度', '考试及格率', '考试优秀率']
        },
        yAxis: [
          {
            type: 'value',
            name: '比例',
            min: 0,
            max: 100,
            interval: 10,
            axisLabel: {
              formatter: '{value} '
            }
          }
        ],
        series: [{
          data: [15, 23, 80, 90, 60],
          type: 'line'
        }]
      }

      option && resource3Chart.setOption(option)
    },
    resourceRes3() {
      console.log('资源图3变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('resource3Chart').offsetWidth
        const h = document.getElementById('resource3Chart').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.resource3Chart.resize(resize)
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
/*.title{*/
/*  font-size: 1rem;*/
/*  font-weight: bold;*/
/*}*/
/*.chartBox {*/
/*  !*margin-top: 0.5rem;*!*/
/*  !*margin-left: 1rem;*!*/
/*  width: 30%;*/
/*  height: 100%;*/
/*  display: inline-block;*/
/*  !*width:calc(100vh / 3*2 - 1.8rem);*!*/
/*  !*height: calc(70vh / 3*2 - 1.8rem);*!*/
/*  !*background-color: skyblue;*!*/
/*}*/
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
.resource1_container {
  width: 67%;
  height: 100%;
  float: left;
  /*background-color: skyblue;*/
}
.resource1_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.resource_title span {
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
  width: 40%;
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
.triangle-right-two {
  width: 0;
  height: 0;
  display: inline-block;
  border-top: 0.5rem solid transparent;
  border-left: 0.8rem solid #e2cd1d;
  border-bottom: 0.5rem solid transparent;
}
.resource2Chart1 {
  /*padding-top: 4%;*/
  width: 100%;
  height: 30%;
  /*background-color: pink;*/
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}
.show_card_container {
  width: 22%;
  height: 60%;
  margin-top: 3%;
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
  font-size: 0.8rem;
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
.resource2Chart2 {
  width: 100%;
  height: 60%;
  /*background-color: #e73466;*/
}
.resource2Chart3 {
  width: 50%;
  height: 100%;
  /*display: inline-block;*/
  float: left;
  /*background-color: #b8e710;*/
}
.resource3_container {
  float: left;
  width: 40%;
  height: 100%;
  /*background-color: #22b0ea;*/
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
  border-left: 0.8rem solid #e21d5b;
  border-bottom: 0.5rem solid transparent;
}
.resource3_chart_container {
  width: 100%;
  height: 88%;
  /*background: #8c939d;*/
}
.resource3Chart {
  width: 100%;
  height: 100%;
}
.resource4_container {
  float: left;
  width: 20%;
  height: 100%;
  /*background-color: #22b0ea;*/
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
.triangle-right-four {
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
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}
.resource4Chart {
  width: 100%;
  height: 100%;
}
.show_card_container_two {
  width: 93%;
  height: 30%;
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
