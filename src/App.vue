<template>

<div id="app" class="layout">
        <Layout>
            <Header>
                <Menu mode="horizontal" theme="dark" active-name="1">
                    <div class="layout-logo"><img src="./assets/logo.png" alt=""></div>
                    <div class="layout-nav">
                        <MenuItem name="1">
                            <!-- <Icon type="ios-navigate"></Icon> -->
                            <img src="./assets/icon2.png" >
                            首页
                        </MenuItem>
                        <MenuItem name="2">
                            <!-- <Icon type="ios-keypad"></Icon> -->
                            <img src="./assets/icon3.png" >
                            告警
                        </MenuItem>
                        <MenuItem name="3">
                            <!-- <Icon type="ios-analytics"></Icon> -->
                            <img src="./assets/icon4.png" >
                            设备
                        </MenuItem>
                        <MenuItem name="4">
                            <!-- <Icon type="ios-paper"></Icon> -->
                            <img src="./assets/icon5.png" >
                            中间性
                        </MenuItem>
                        <div style="float:right">
                          <MenuItem name="3">
                            <!-- <Icon type="ios-analytics"></Icon> -->
                            <img src="./assets/icon6.png" >
                            Admin
                        </MenuItem>
                        <MenuItem name="4">
                            <!-- <Icon type="ios-paper"></Icon> -->
                            <img src="./assets/icon7.png" >
                            退出
                        </MenuItem>
                        </div>
                    </div>
                </Menu>
            </Header>
            <Layout>
                <Sider hide-trigger :style="{background: '#fff'}">
                    <Menu active-name="1-2" theme="light" width="auto" :open-names="['1']">
                        <Submenu name="1">
                            <template slot="title">
                                <!-- <Icon type="ios-navigate"></Icon> -->
                                <img src="./assets/icon1.png" >
                                设备数据大平台
                            </template>
                        </Submenu>
                        <Submenu name="2">
                            <template slot="title">
                                <!-- <Icon type="ios-keypad"></Icon> -->
                                 <img src="./assets/icon.png" >
                                视频监控
                            </template>
                            <MenuItem name="2-1">SIP会议室</MenuItem>
                            <MenuItem name="2-2">前仿会议室</MenuItem>
                            <MenuItem name="2-3">JSC326会议室 </MenuItem>
                        </Submenu>
                       
                    </Menu>
                </Sider>
                <Layout :style="{padding: '0 25px'}">
                   
                    <Content :style="{padding: '24px 0', minHeight: '280px'}">
                         <router-view style="width:100%"/>
                    </Content>
                </Layout>
            </Layout>
        </Layout>
    </div>
  <!-- <div id="app">
    
    <router-view/>
  </div> -->
</template>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
} */

html,body{
  height: 100%;
}

.layout{
    border: 1px solid #d7dde4;
    position: relative;
    border-radius: 4px;
    overflow: hidden;
    height: 100%;
    background: url("./assets/bj.png") no-repeat !important;
    background-size: 100% 100% !important;
}
.ivu-layout{
  height: 100%;
  background: none !important;
}
.ivu-layout-header{
  padding: 0 !important;
  background: none !important;
  height: auto !important;
}
.ivu-menu-dark{
  background: rgba(0, 0, 0, .4) !important;
}
.ivu-menu-vertical .ivu-menu-item:hover, .ivu-menu-vertical .ivu-menu-submenu-title:hover,.ivu-menu{
  color: #fff !important;
}
.ivu-menu-light.ivu-menu-vertical .ivu-menu-item-active:not(.ivu-menu-submenu){
  background:rgba(0, 0, 0, .5) !important;
  color: #fff !important;
}
.ivu-menu-submenu-title{
  display: flex !important;
  align-items: center;
}
.ivu-menu-item{
  display: flex !important;
  align-items: center;
  justify-content: center;
}
.ivu-menu-submenu-title img{
  margin-right: 15px;
}
.ivu-menu-item img{
  margin-right: 15px;
}
.ivu-layout-sider{
  width: 245px !important;
  min-width: 245px !important;
  max-width: 245px !important;
  flex: 0 0 245px !important;
  background: rgba(0, 0, 0, .3) !important;
}
.ivu-menu-light{
  background: rgba(0,0,0,.4) !important;
  color: #fff !important;
}
.layout-logo{
    width: 245px;
    height: 60px;
    background: #273749;
    float: left;
    position: relative;
    top: 0px;
    left: 0px;
    display: flex;
    align-items: center;
    justify-content: center;
}
.layout-nav{
    width: auto;
    margin: 0 auto;
}
</style>
