<template>
  <div class="all_container">
    <Header style="width: 100%;height: 12%" />
    <!--    <div style="padding-top: 1rem">-->
    <!--      &lt;!&ndash;      <span class="title">这是大屏页面</span>&ndash;&gt;-->
    <!--      &lt;!&ndash;      <el-button type="primary" round @click="gotoManagementPlatform">点击跳转回管理平台</el-button>&ndash;&gt;-->
    <!--    </div>-->
    <!--    <h1>这是大屏页面</h1>-->
    <!--    <el-button type="primary" round @click="gotoManagementPlatform">点击跳转回管理平台</el-button>-->
    <!--    <div style="width: 100%;height: 30%">-->
    <!--      <div class="chartBox">-->
    <!--        <div class="echart_container">-->
    <!--          <div id="myChart6" style="height: 100%;width: 100%" />-->
    <!--        </div>-->
    <!--      </div>-->
    <!--      <div class="chartBox">-->
    <!--        <div class="echart_container">-->
    <!--          <div id="myChart7" style="height: 100%;width: 100%" />-->
    <!--        </div>-->
    <!--      </div>-->
    <!--    </div>-->
    <div style="width: 100%;height: 44%;">
      <div class="cure_container">
        <div class="cure_title">
          <div class="triangle-right" />
          <span>校园核心数据展示</span>
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
      <div class="teacher_container">
        <div class="tea_title">
          <div class="triangle-right-two" />
          <span>师资队伍</span>
        </div>
        <div class="tea_content">
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>139</span>
            </div>
            <div class="tea_two_layer">
              <span>专任教师数量</span>
            </div>
          </div>
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>41</span>
            </div>
            <div class="tea_two_layer">
              <span>校外兼职教师数量</span>
            </div>
          </div>
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>32</span>
            </div>
            <div class="tea_two_layer">
              <span>校内兼课教师数量</span>
            </div>
          </div>
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>13</span>
            </div>
            <div class="tea_two_layer">
              <span>校外兼课教师数量</span>
            </div>
          </div>
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>13%</span>
            </div>
            <div class="tea_two_layer">
              <span>高级职务教师比例</span>
            </div>
          </div>
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>23%</span>
            </div>
            <div class="tea_two_layer">
              <span>研究生学历教师比例</span>
            </div>
          </div>
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>54</span>
            </div>
            <div class="tea_two_layer">
              <span>高层次人才数量</span>
            </div>
          </div>
          <div class="tea_item">
            <div class="tea_one_layer">
              <span>28</span>
            </div>
            <div class="tea_two_layer">
              <span>双师素质教师人数</span>
            </div>
          </div>
        </div>
      </div>
      <div class="chart_container">
        <div class="chart_one_layer">
          <div class="teaChartOne">
            <div class="echart_container">
              <div id="teacherOne" style="height: 100%;width: 100%" />
            </div>
          </div>
          <div class="teaChartOne">
            <div class="echart_container">
              <div id="teacherTwo" style="height: 100%;width: 100%" />
            </div>
          </div>
          <div class="teaChartOne">
            <div class="echart_container">
              <div id="teacherThree" style="height: 100%;width: 100%" />
            </div>
          </div>
        </div>
        <div class="chart_two_layer">
          <div class="teaChartTwo">
            <div class="echart_container">
              <div id="teacherFour" style="height: 100%;width: 100%" />
            </div>
          </div>
          <div class="teaChartTwo">
            <div class="echart_container">
              <div id="teacherFive" style="height: 100%;width: 100%" />
            </div>
          </div>
          <div class="teaChartTwo">
            <div class="echart_container">
              <div id="teacherSix" style="height: 100%;width: 100%" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <div style="width: 100%;height: 44%;">
      <div class="teawork_container">
        <div class="work_title">
          <div class="triangle-right-three" />
          <span>教学工作</span>
        </div>
        <div class="work_chart_container">
          <div class="workChartOne">
            <div class="echart_container">
              <div id="workChart" style="height: 100%;width: 100%" />
            </div>
          </div>
        </div>
      </div>
      <div class="student_container">
        <div class="student_title">
          <div class="triangle-right-four" />
          <span>招生情况</span>
        </div>
        <div class="student_chart_container">
          <div class="studnetChartOne">
            <div class="echart_container">
              <div id="studentChart" style="height: 100%;width: 100%;" />
            </div>
          </div>
        </div>
      </div>
      <div class="asset_container">
        <div class="asset_title">
          <div class="triangle-right-five" />
          <span>资产情况</span>
        </div>
        <div class="asset_chart_container">
          <div class="studnetChartThree">
            <div class="echart_container">
              <div id="assetChartOne" style="height: 100%;width: 100%;" />
            </div>
          </div>
        </div>
        <div class="asset_chart_container">
          <div class="studnetChartThree">
            <div class="echart_container">
              <div id="assetChartTwo" style="height: 100%;width: 100%;" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/views/myComponents/head/header'
import vueSeamlessScroll from 'vue-seamless-scroll'
export default {
  name: 'Index',
  components: {
    Header,
    vueSeamlessScroll
  },
  data() {
    return {
      CardPartsStatisticsList: [
        {
          name: '建筑面积',
          number: '234522',
          targetNumber: '260000',
          warnNumber: '100323',
          danwei: '平米'
        },
        { name: '师生比',
          number: '12',
          targetNumber: '10',
          warnNumber: '7',
          danwei: '%' },
        { name: '横向技术到款额',
          number: '103',
          targetNumber: '111',
          warnNumber: '45',
          danwei: '万元' },
        { name: '纵向技术到款额',
          number: '200',
          targetNumber: '150',
          warnNumber: '100',
          danwei: '万元' },
        { name: '生均教学用房面积',
          number: '45',
          targetNumber: '60',
          warnNumber: '23',
          danwei: '平米' },
        { name: '生均财政拨水平',
          number: '1',
          targetNumber: '1.2',
          warnNumber: '0.8',
          danwei: '万元' },
        // { name: '建筑面积',
        //   number: '234522',
        //   targetNumber: '111',
        //   warnNumber: '100323',
        //   danwei: '平米' },
        { name: '多媒体教室数',
          number: '57',
          targetNumber: '80',
          warnNumber: '23',
          danwei: '间' },
        { name: '生均图书册数',
          number: '134',
          targetNumber: '100',
          warnNumber: '65',
          danwei: '册' },
        { name: '生均仪器设置值',
          number: '15',
          targetNumber: '10',
          warnNumber: '5',
          danwei: '只' },
        { name: '新增科研仪器占比',
          number: '23',
          targetNumber: '30',
          warnNumber: '12',
          danwei: '%' }
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
    this.initTeacher1()
    this.teacher1Res()
    this.initTeacher2()
    this.teacher2Res()
    this.initTeacher3()
    this.teacher3Res()
    this.initTeacher4()
    this.teacher4Res()
    this.initTeacher5()
    this.teacher5Res()
    this.initTeacher6()
    this.teacher6Res()
    // this.initmyChart6()
    // this.chart6Res()
    // this.initmyChart7()
    // this.chart7Res()
    this.initWork1()
    this.work1Res()
    this.initStudent1()
    this.student1Res()
    this.initAsset1()
    this.asset1Res()
    this.initAsset2()
    this.asset2Res()
  },
  methods: {
    gotoManagementPlatform: function() {
      this.$router.push('/documentation/index')
    },
    initmyChart6() {
      console.log('测试')
      this.myChart6 = this.$echarts.init(document.getElementById('myChart6'), 'light')
      var option = {
        // backgroundColor: "#0f375f",
        legend: {
          orient: 'vertical',
          top: 'center',
          right: '5%',
          data: ['省级流域', '市级流域', '县级流域', '镇级流域'],
          textStyle: {
            color: '#fff',
            fontSize: 16
          }
        },
        tooltip: {
          trigger: 'item',
          formatter: '{a} <br/>{b} : {c} ({d}%)'
        },
        series: [{
          name: '分布情况',
          type: 'pie',
          radius: ['30%', '60%'],
          center: ['40%', '50%'],
          roseType: 'radius',
          label: {
            show: true,
            normal: {
              position: 'outside',
              fontSize: 16
            }
          },
          labelLine: {
            length: 1,
            length2: 20,
            smooth: true
          },
          data: [{
            value: 1,
            name: '省级流域',
            itemStyle: {
              color: 'rgba(50,123,250,0.7)',
              borderColor: 'rgba(50,123,250,1)',
              borderWidth: 3
            }
          },
          {
            value: 5,
            name: '市级流域',
            itemStyle: {
              color: 'rgba(244,201,7,0.7)',
              borderColor: 'rgba(244,201,7,1)',
              borderWidth: 3
            }
          },
          {
            value: 12,
            name: '县级流域',
            itemStyle: {
              color: 'rgba(23,216,161,0.7)',
              borderColor: 'rgba(23,216,161,1)',
              borderWidth: 3
            }
          },
          {
            value: 24,
            name: '镇级流域',
            itemStyle: {
              color: 'rgba(122,60,235,0.7)',
              borderColor: 'rgba(122,60,235,1)',
              borderWidth: 3
            }
          }
          ]
        }]
      }
      this.myChart6.setOption(option)
    },
    chart6Res() {
      console.log('测试2')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('myChart6').offsetWidth
        const h = document.getElementById('myChart6').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.myChart6.resize(resize)
        }, 100)
      })
    },
    initmyChart7() {
      console.log('测试')
      this.myChart7 = this.$echarts.init(document.getElementById('myChart7'), 'light')
      var option = {
        // backgroundColor: "#0f375f",
        legend: {
          orient: 'vertical',
          top: 'center',
          right: '5%',
          data: ['省级流域', '市级流域', '县级流域', '镇级流域'],
          textStyle: {
            color: '#fff',
            fontSize: 16
          }
        },
        tooltip: {
          trigger: 'item',
          formatter: '{a} <br/>{b} : {c} ({d}%)'
        },
        series: [{
          name: '分布情况',
          type: 'pie',
          radius: ['30%', '60%'],
          center: ['40%', '50%'],
          roseType: 'radius',
          label: {
            show: true,
            normal: {
              position: 'outside',
              fontSize: 16
            }
          },
          labelLine: {
            length: 1,
            length2: 20,
            smooth: true
          },
          data: [{
            value: 1,
            name: '省级流域',
            itemStyle: {
              color: 'rgba(50,123,250,0.7)',
              borderColor: 'rgba(50,123,250,1)',
              borderWidth: 3
            }
          },
          {
            value: 5,
            name: '市级流域',
            itemStyle: {
              color: 'rgba(244,201,7,0.7)',
              borderColor: 'rgba(244,201,7,1)',
              borderWidth: 3
            }
          },
          {
            value: 12,
            name: '县级流域',
            itemStyle: {
              color: 'rgba(23,216,161,0.7)',
              borderColor: 'rgba(23,216,161,1)',
              borderWidth: 3
            }
          },
          {
            value: 24,
            name: '镇级流域',
            itemStyle: {
              color: 'rgba(122,60,235,0.7)',
              borderColor: 'rgba(122,60,235,1)',
              borderWidth: 3
            }
          }
          ]
        }]
      }
      this.myChart7.setOption(option)
    },
    chart7Res() {
      console.log('测试2')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('myChart7').offsetWidth
        const h = document.getElementById('myChart7').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.myChart7.resize(resize)
        }, 100)
      })
    },
    initTeacher1() {
      console.log('生成教师图1')
      this.teacherOne = this.$echarts.init(document.getElementById('teacherOne'), 'light')
      var option = {
        title: {
          text: '教师职称结构',
          top: '10',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        // legend: {
        //   orient: 'vertical',
        //   left: 'left'
        // },
        series: [
          {
            name: '职称',
            type: 'pie',
            radius: '50%',
            data: [
              { value: 1048, name: '正高' },
              { value: 735, name: '副高' },
              { value: 580, name: '中级' },
              { value: 484, name: '初级' }
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
      this.teacherOne.setOption(option)
    },
    teacher1Res() {
      console.log('教师图1变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('teacherOne').offsetWidth
        const h = document.getElementById('teacherOne').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.teacherOne.resize(resize)
        }, 100)
      })
    },
    initTeacher2() {
      console.log('生成教师图2')
      this.teacherTwo = this.$echarts.init(document.getElementById('teacherTwo'), 'light')
      var option = {
        title: {
          text: '教师年龄结构',
          top: '10',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        // legend: {
        //   orient: 'vertical',
        //   left: 'left'
        // },
        series: [
          {
            name: '年龄',
            type: 'pie',
            radius: '50%',
            data: [
              { value: 22, name: '35岁以下' },
              { value: 54, name: '36-60岁' },
              { value: 34, name: '60岁以上' }
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
      this.teacherTwo.setOption(option)
    },
    teacher2Res() {
      console.log('教师图1变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('teacherTwo').offsetWidth
        const h = document.getElementById('teacherTwo').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.teacherTwo.resize(resize)
        }, 100)
      })
    },
    initTeacher3() {
      console.log('生成教师图3')
      this.teacherThree = this.$echarts.init(document.getElementById('teacherThree'), 'light')
      var option = {
        title: {
          text: '教师学历结构',
          top: '10',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        // legend: {
        //   orient: 'vertical',
        //   left: 'left'
        // },
        series: [
          {
            name: '学历',
            type: 'pie',
            radius: '50%',
            data: [
              { value: 34, name: '研究生' },
              { value: 75, name: '本科' },
              { value: 10, name: '大专' },
              { value: 8, name: '中专' }
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
      this.teacherThree.setOption(option)
    },
    teacher3Res() {
      console.log('教师图3变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('teacherThree').offsetWidth
        const h = document.getElementById('teacherThree').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.teacherThree.resize(resize)
        }, 100)
      })
    },
    initTeacher4() {
      console.log('生成教师图4')
      this.teacherFour = this.$echarts.init(document.getElementById('teacherFour'), 'light')
      var option = {
        title: {
          text: '教师性别结构',
          top: '10',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        // legend: {
        //   orient: 'vertical',
        //   left: 'left'
        // },
        series: [
          {
            name: '性别',
            type: 'pie',
            radius: '50%',
            data: [
              { value: 68, name: '男' },
              { value: 56, name: '女' }
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
      this.teacherFour.setOption(option)
    },
    teacher4Res() {
      console.log('教师图4变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('teacherFour').offsetWidth
        const h = document.getElementById('teacherFour').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.teacherFour.resize(resize)
        }, 100)
      })
    },
    initTeacher5() {
      console.log('生成教师图5')
      this.teacherFive = this.$echarts.init(document.getElementById('teacherFive'), 'light')
      var option = {
        title: {
          text: '教师学位结构',
          top: '10',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        // legend: {
        //   orient: 'vertical',
        //   left: 'left'
        // },
        series: [
          {
            name: '学位',
            type: 'pie',
            radius: '50%',
            data: [
              { value: 7, name: '博士' },
              { value: 23, name: '硕士' },
              { value: 56, name: '学士' },
              { value: 12, name: '其他' }
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
      this.teacherFive.setOption(option)
    },
    teacher5Res() {
      console.log('教师图5变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('teacherFive').offsetWidth
        const h = document.getElementById('teacherFive').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.teacherFive.resize(resize)
        }, 100)
      })
    },
    initTeacher6() {
      console.log('生成教师图6')
      this.teacherSix = this.$echarts.init(document.getElementById('teacherSix'), 'light')
      var option = {
        title: {
          text: '教师类型结构',
          top: '10',
          left: 'center',
          textStyle: {
            fontSize: '15'
          },
          color: '#44a5fc'
        },
        tooltip: {
          trigger: 'item'
        },
        // legend: {
        //   orient: 'vertical',
        //   left: 'left'
        // },
        series: [
          {
            name: '类型',
            type: 'pie',
            radius: '50%',
            data: [
              { value: 139, name: '专任' },
              { value: 23, name: '兼职' },
              { value: 43, name: '兼课' }
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
      this.teacherSix.setOption(option)
    },
    teacher6Res() {
      console.log('教师图6变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('teacherSix').offsetWidth
        const h = document.getElementById('teacherSix').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.teacherSix.resize(resize)
        }, 100)
      })
    },
    initWork1() {
      console.log('生成工作图1')
      this.workChart = this.$echarts.init(document.getElementById('workChart'), 'light')
      var option = {
        // title: {
        //   text: '世界人口总量',
        //   subtext: '数据来自网络'
        // },
        tooltip: {
          trigger: 'axis',
          axisPointer: {
            type: 'shadow'
          }
        },
        legend: {
          data: ['2020年']
        },
        grid: {
          left: '3%',
          right: '4%',
          bottom: '3%',
          containLabel: true
        },
        xAxis: {
          type: 'value',
          boundaryGap: [0, 0.01]
        },
        yAxis: {
          type: 'category',
          data: ['人均课时', '专任教师人均课时', '教材总数', '规划教材总数', '校内实训基地数量', '校外实训基地数量', '顶岗实习人数']
        },
        series: [
          {
            name: '2011年',
            type: 'bar',
            data: [400, 280, 29000, 24000, 40, 80, 12000]
          }
        ]
      }
      this.workChart.setOption(option)
    },
    work1Res() {
      console.log('工作图1变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('workChart').offsetWidth
        const h = document.getElementById('workChart').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.workChart.resize(resize)
        }, 100)
      })
    },
    initStudent1() {
      console.log('生成学生图1')
      this.studentChart = this.$echarts.init(document.getElementById('studentChart'), 'light')
      var option = {
        tooltip: {
          trigger: 'axis',
          axisPointer: {
            type: 'cross',
            crossStyle: {
              color: '#999'
            }
          }
        },
        toolbox: {
          feature: {
            dataView: { show: true, readOnly: false },
            magicType: { show: true, type: ['line', 'bar'] },
            restore: { show: true },
            saveAsImage: { show: true }
          }
        },
        legend: {
          data: ['2020年', '2019年', '招生专业数量']
        },
        xAxis: [
          {
            type: 'category',
            data: ['省内生源数量', '省外生源数量', '单招人数', '普招人数', '计划招生人数', '实际录取人数', '实际报道人数'],
            axisPointer: {
              type: 'shadow'
            }
          }
        ],
        yAxis: [
          {
            type: 'value',
            name: '人数',
            min: 0,
            max: 2000,
            interval: 200
            // axisLabel: {
            //   formatter: '{value} ml'
            // }
          },
          {
            type: 'value',
            name: '数量',
            min: 0,
            max: 25,
            interval: 5
            // axisLabel: {
            //   formatter: '{value} °C'
            // }
          }
        ],
        series: [
          {
            name: '2020年',
            type: 'bar',
            data: [1600, 400, 784, 942, 1845, 1632, 1616]
          },
          {
            name: '2019年',
            type: 'bar',
            data: [1743, 345, 800, 670, 1748, 1457, 1400]
          },
          {
            name: '招生专业数量',
            type: 'line',
            yAxisIndex: 1,
            data: [20, 22, 20, 21, 23, 23, 23, 24]
          }
        ]
      }
      this.studentChart.setOption(option)
    },
    student1Res() {
      console.log('学生图1变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('studentChart').offsetWidth
        const h = document.getElementById('studentChart').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.studentChart.resize(resize)
        }, 100)
      })
    },
    initAsset1() {
      console.log('生成学生图1')
      this.assetChartOne = this.$echarts.init(document.getElementById('assetChartOne'), 'light')
      var option = {
        xAxis: {
          type: 'category',
          data: ['生均占地面积', '生均教学行政用房', '生均宿舍面积', '生均实践场所']
          //   axisLabel: {// 坐标轴刻度标签的相关设置。
          //     clickable: true, // 并给图表添加单击事件  根据返回值判断点击的是哪里
          //     interval: 0,
          //     formatter: function(params, index) {
          //       if (index % 2 !== 0) {
          //         return '\n\n' + params
          //       } else {
          //         return params
          //       }
          //     }
          //   }
        },
        tooltip: {
          trigger: 'axis'
        },
        yAxis: {
          type: 'value',
          axisLabel: {
            formatter: '{value} m/s'
          }
        },
        series: [{
          data: [150, 230, 224, 218],
          type: 'line'
        }]
      }
      this.assetChartOne.setOption(option)
    },
    asset1Res() {
      console.log('学生图1变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('assetChartOne').offsetWidth
        const h = document.getElementById('assetChartOne').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.assetChartOne.resize(resize)
        }, 100)
      })
    },
    initAsset2() {
      console.log('生成资产图')
      this.assetChartTwo = this.$echarts.init(document.getElementById('assetChartTwo'), 'light')
      var option = {
        xAxis: {
          type: 'category',
          data: ['生均校内实践教学工位数', '百名学生配多媒体教室座位数', '百名学生配教学用计算机数', '生均图书']
        },
        tooltip: {
          trigger: 'axis'
        },
        yAxis: {
          type: 'value',
          axisLabel: {
            formatter: '{value} 台/本'
          }
        },
        series: [{
          data: [10, 2, 2, 18],
          type: 'line'
        }]
      }
      this.assetChartTwo.setOption(option)
    },
    asset2Res() {
      console.log('资产图变形')
      const _this = this
      window.addEventListener('resize', function() {
        const w = document.getElementById('assetChartTwo').offsetWidth
        const h = document.getElementById('assetChartTwo').offsetHeight
        const resize = {
          width: w,
          height: h
        }
        // _this.myChart1.resize();
        setTimeout(() => {
          _this.assetChartTwo.resize(resize)
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
.teacher_container {
  width: 33%;
  height: 100%;
  float: left;
  /*background-color: skyblue;*/
}
.tea_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.tea_title span {
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
.tea_content {
  width: 100%;
  height: 90%;
  display: flex;
  flex-wrap: wrap;
  margin-top: 1.5rem;
  margin-left: 2rem;
}
.tea_item {
  width: 28%;
  height: 5rem;
  justify-content: center;
  /*background-color: #2ac06d;*/
}
.tea_one_layer {
  height: 3rem;
  text-align: center;
}
.tea_one_layer span {
  line-height: 3rem;
  font-size: 2rem;
  font-weight: bold;
  color:#44a5fc ;
}
.tea_two_layer {
  height: 2rem;
  text-align: center;
}
.tea_two_layer span {
  display: inline-block;
  border-radius: 1rem;
  background-color: #bedee3;
  width: 80%;
  height: 1.5rem;
  line-height: 1.5rem;
  color: #23252a;
  font-size: 0.7rem;
}
.chart_container {
  width: 34%;
  height: 100%;
  float: left;
  /*background-color: skyblue;*/
}
.chart_one_layer {
  width: 100%;
  height: 50%;
  /*background: pink;*/
}
.teaChartOne {
  width: 32%;
  height: 100%;
  display: inline-block;
}
.chart_two_layer {
  width: 100%;
  height: 50%;
  /*background: green;*/
}
.teaChartTwo {
  width: 32%;
  height: 100%;
  display: inline-block;
}
.teawork_container {
  float: left;
  width: 33%;
  height: 100%;
  /*background-color: skyblue;*/
}
.work_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.work_title span {
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
.work_chart_container {
  width: 100%;
  height: 88%;
  /*background: #8c939d;*/
}
.workChartOne {
  width: 100%;
  height: 100%;
}
.student_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.student_title span {
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
.student_chart_container {
  width: 100%;
  height: 88%;
  /*background: #8c939d;*/
}
.studnetChartOne {
  width: 100%;
  height: 100%;
}
.student_container {
  float: left;
  width: 33%;
  height: 100%;
  /*background-color: skyblue;*/
}
.asset_container {
  float: left;
  width: 33%;
  height: 100%;
  /*background-color: skyblue;*/
}
.asset_title {
  margin-left: 1rem;
  padding-top: 1rem;
}
.asset_title span {
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
  border-left: 0.8rem solid #901de2;
  border-bottom: 0.5rem solid transparent;
}
.asset_chart_container {
  width: 100%;
  height: 45%;
  /*background-color: yellow;*/
}
.studnetChartThree {
  width: 100%;
  height: 100%;
}
</style>
