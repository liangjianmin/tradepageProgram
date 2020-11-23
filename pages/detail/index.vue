<template>
    <view class="detail">
        <view class="h-head row verCenter">
            <view class="search-box row bothSide">
                <view class="search-bar row verCenter">
                    <view class="country row verCenter">
                        <text class="arrow"></text>
                        <text class="txt">CHN 中国</text>
                    </view>
                    <input type="text" class="inp" :value="name" placeholder="请输入企业名称关键词" placeholder-style="color:#999999;"/>
                </view>
                <view class="btn row rowCenter verCenter">查一下</view>
            </view>
        </view>
        <!-- 企业名称 -->
        <template v-if="type == 1 || type == 2">
            <view class="collection column">
                <text class="t1">Sample Company</text>
                <view class="list row">
                    <view class="box color1 row rowCenter verCenter">国别风险高</view>
                    <view class="box color1 row rowCenter verCenter">主权信用风险高</view>
                    <view class="box color2 row rowCenter verCenter">主权信用风险中</view>
                    <view class="box color3 row rowCenter verCenter">主权信用风险低</view>
                </view>
                <text class="t2">外贸护法企业编号：INDDUNSNUMBER</text>
                <text class="t3">信息更新时间：2019年10月1日；</text>
                <view class="btn-box row">
                    <view class="btn row rowCenter verCenter">收藏企业</view>
                </view>
            </view>
        </template>

        <template v-if="type == 3">
            <view class="collection column">
                <text class="t1">Apple Inc.</text>
                <text class="t2">外贸护法企业编号：INDDUNSNUMBER</text>
                <text class="t3">信息更新时间：2020年11月16日；</text>
                <view class="btn-box row">
                    <view class="btn row rowCenter verCenter">收藏企业</view>
                </view>
            </view>
        </template>

        <template v-if="type == 4">
            <view class="collection column">
                <text class="t1">Google LLC</text>
                <view class="list row">
                    <view class="box color1 row rowCenter verCenter">无财务信息</view>
                </view>
                <text class="t2">外贸护法企业编号：INDDUNSNUMBER</text>
                <text class="t3">信息更新时间：2020年11月16日；</text>
                <view class="btn-box row">
                    <view class="btn row rowCenter verCenter">收藏企业</view>
                </view>
            </view>
        </template>
        <view class="title row rowCenter verCenter" style="width: 150rpx;">基本信息</view>
        <!-- 基本信息 -->
        <template v-if="type == 1 || type == 2">
            <view class="baseinfo">
                <view class="show-data row">
                    <view class="box column">
                        <text class="t1">注册编号</text>
                        <text class="t2">1234567890123</text>
                        <text class="t1">营业日期</text>
                        <text class="t2">2001年1月1日</text>
                        <text class="t1">电话</text>
                        <text class="t2">+65 0324 7514</text>
                        <text class="t1">员工数量</text>
                        <text class="t2">2000</text>
                    </view>
                    <view class="box column ml">
                        <text class="t1">经营状态</text>
                        <text class="color1">存续</text>
                        <text class="t1">国别/地区</text>
                        <text class="t2">印度</text>
                        <text class="t1">国家风险评级</text>
                        <view class="risk row verCenter">
                            <text class="num row rowCenter verCenter">8</text>
                            <text class="tt">高风险</text>
                            <text class="iconfont icontishi"></text>
                        </view>
                        <text class="t1">国家主权信用风险评级</text>
                        <view class="risk row verCenter">
                            <text class="num row rowCenter verCenter">C</text>
                            <text class="tt">高风险</text>
                            <text class="iconfont icontishi"></text>
                        </view>
                    </view>
                </view>
                <view class="bar column">
                    <text class="t1">经营地址</text>
                    <text class="t2">C-7/227, Second Floor Sector-7, Rohini Delhi USA,Unite State</text>
                    <text class="t1">注册地址</text>
                    <text class="t2">C-7/227, Second Floor Sector-7, Rohini Delhi USA,Unite State</text>
                    <text class="t1">主营业务</text>
                    <text class="t2">手机批发(SIC：12345678)；手机零售(SIC：87654321)</text>
                </view>
                <view class="risk-error">
                    <view class="tit">风险提示</view>
                    <view class="list">
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">1</view>
                            <view class="txt">
                                企业状态：
                                <text class="t1">非存续</text>
                                ，高危提示！
                            </view>
                        </view>
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">2</view>
                            <view class="txt">
                                国别风险：
                                <text class="t2">8</text>
                                政治和经济形势不稳定，商业环境不太好，国家风险水平较高。
                            </view>
                        </view>
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">3</view>
                            <view class="txt">
                                国家主权风险：
                                <text class="t2">C</text>
                                主权债务规模最高，主权债务可持续性最差，主权信用风险水平最高。
                            </view>
                        </view>
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">4</view>
                            <view class="txt">员工数量：为3，慎防空壳公司。</view>
                        </view>
                    </view>
                </view>
            </view>
        </template>
        <template v-else-if="type == 3">
            <view class="baseinfo">
                <view class="show-data row">
                    <view class="box column">
                        <text class="t1">注册编号</text>
                        <text class="t2">C0806592</text>
                        <text class="t1">营业日期</text>
                        <text class="t2">1977年1月3日</text>
                        <text class="t1">电话</text>
                        <text class="t2">+1 408-996-1010</text>
                        <text class="t1">员工数量</text>
                        <text class="t2">147000</text>
                    </view>
                    <view class="box column ml">
                        <text class="t1">经营状态</text>
                        <text class="color1">存续</text>
                        <text class="t1">国别/地区</text>
                        <text class="t2">美国 USA</text>
                        <text class="t1">国家风险评级</text>
                        <view class="risk row verCenter">
                            <text class="num row rowCenter verCenter" style="color:#5FC85E;">2</text>
                            <text class="tt" style="color:#5FC85E;">低风险</text>
                        </view>
                        <text class="t1">国家主权信用风险评级</text>
                        <view class="risk row verCenter">
                            <text class="num row rowCenter verCenter" style="color:#5FC85E;">AAA</text>
                            <text class="tt" style="color:#5FC85E;">低风险</text>
                            <text class="iconfont icontishi"></text>
                        </view>
                    </view>
                </view>
                <view class="bar column">
                    <text class="t1">经营地址</text>
                    <text class="t2">1 Apple Park Way, Cupertino, CA, 95014, UNITED STATES</text>
                    <text class="t1">注册地址</text>
                    <text class="t2">California</text>
                    <text class="t1">主营业务</text>
                    <text class="t2">制造广播/电视通讯设备(SIC:3663)；移动通讯设备(SIC:36639906)；个人电脑，微型计算机(SIC:35719904)；电脑终端，显示器和组件(SIC:35750100)；打印机，电脑(SIC:35770102)；声音还原设备(SIC:36510118)；操作系统计算机软件(SIC:73729905)；应用计算机软件(SIC:73729901)；</text>
                </view>
            </view>
        </template>
        <template v-else-if="type == 4">
            <view class="baseinfo">
                <view class="show-data row">
                    <view class="box column">
                        <text class="t1">注册编号</text>
                        <text class="t2">-</text>
                        <text class="t1">注册日期</text>
                        <text class="t2">2002年10月22日</text>
                        <text class="t1">电话</text>
                        <text class="t2">+65 0324 7514</text>
                        <text class="t1">员工数量</text>
                        <text class="t2">61814</text>
                    </view>
                    <view class="box column ml">
                        <text class="t1">经营状态</text>
                        <text class="color1">存续</text>
                        <text class="t1">国别/地区</text>
                        <text class="t2">美国 USA</text>
                        <text class="t1">国家风险评级</text>
                        <view class="risk row verCenter">
                            <text class="num row rowCenter verCenter" style="color:#5FC85E;">2</text>
                            <text class="tt" style="color:#5FC85E;">低风险</text>
                        </view>
                        <text class="t1">国家主权信用风险评级</text>
                    </view>
                </view>
            </view>
            <view class="bar column">
                <text class="t1">经营地址</text>
                <text class="t2">1600 Amphitheatre Pkwy, Mountain View, CA, 94043, UNITED STATES</text>
                <text class="t1">注册地址</text>
                <text class="t2">CDelaware</text>
                <text class="t1">主营业务</text>
                <text class="t2">定制电脑程序(SIC：7371)；电脑软件开发(SIC：73710301)；数据库信息检索(SIC：73759901)</text>
            </view>
        </template>
        <!-- 经营信息 -->
        <view class="title row rowCenter verCenter" style="width: 145rpx;">经营信息</view>
        <template v-if="type == 1">
            <view class="business-information">
                <navigator url="/pages/user/buy" hover-class="none">
                    <image src="../../static/fj.png" mode="aspectFill" class="business-bggg"></image>
                </navigator>
                <view class="table">
                    <view class="box row">
                        <view class="left row rowCenter verCenter">财务日期</view>
                        <view class="right row rowCenter verCenter">2009年3月27日 — 2020年12月27日</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">营业收入</view>
                        <view class="right row rowCenter verCenter">$45,458.00（微型企业）</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">是否进口商</view>
                        <view class="right row rowCenter verCenter">是</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">风险诉讼记录</view>
                        <view class="right row rowCenter verCenter">12</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">累计利润</view>
                        <view class="right row rowCenter verCenter">1212</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">当年净利润</view>
                        <view class="right xf row rowCenter verCenter"></view>
                    </view>
                </view>
                <view class="risk-error">
                    <view class="tit">风险提示</view>
                    <view class="list">
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">1</view>
                            <view class="txt">
                                <text>该企业无披露财务数据，注意企业兑付能力与采购能力。点击使用</text>
                                <text @click="toUrl()" class="link" hover-class="none">企业信用报告</text>
                                <text>获取更多内容。</text>
                            </view>
                        </view>
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">2</view>
                            <view class="txt">该企业为小（微）企业，注意企业兑付能力与采购能力</view>
                        </view>
                    </view>
                </view>
            </view>
        </template>
        <template v-else-if="type == 2">
            <view class="business-information-sb">
                <view class="business-information-bg">
                    <navigator class="bg" url="/pages/user/login" hover-class="none" style="top: 33rpx;right: 33rpx;"></navigator>
                </view>
            </view>
        </template>
        <template v-else-if="type == 3">
            <view class="business-information">
                <navigator url="/pages/user/buy" hover-class="none">
                    <image src="../../static/fj.png" mode="aspectFill" class="business-bggg"></image>
                </navigator>
                <view class="table">
                    <view class="box row">
                        <view class="left row rowCenter verCenter">财务日期</view>
                        <view class="right row rowCenter verCenter">2019年9月29日-2020年9月26日</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">营业收入</view>
                        <view class="right row rowCenter verCenter">$ 274,515,000,000.00 (大型企业）</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">是否进口商</view>
                        <view class="right row rowCenter verCenter">-</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">风险诉讼记录</view>
                        <view class="right row rowCenter verCenter">12</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">累计利润</view>
                        <view class="right row rowCenter verCenter">1212</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">当年净利润</view>
                        <view class="right xf row rowCenter verCenter"></view>
                    </view>
                </view>
            </view>
        </template>
        <template v-else-if="type == 4">
            <view class="business-information">
                <navigator url="/pages/user/buy" hover-class="none">
                    <image src="../../static/fj.png" mode="aspectFill" class="business-bggg"></image>
                </navigator>
                <view class="table">
                    <view class="box row">
                        <view class="left row rowCenter verCenter">财务日期</view>
                        <view class="right row rowCenter verCenter">-</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">营业收入</view>
                        <view class="right row rowCenter verCenter">-</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">是否进口商</view>
                        <view class="right row rowCenter verCenter">-</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">风险诉讼记录</view>
                        <view class="right row rowCenter verCenter">12</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">累计利润</view>
                        <view class="right row rowCenter verCenter">1212</view>
                    </view>
                    <view class="box row">
                        <view class="left row rowCenter verCenter">当年净利润</view>
                        <view class="right xf row rowCenter verCenter"></view>
                    </view>
                </view>
                <view class="risk-error">
                    <view class="tit">风险提示</view>
                    <view class="list">
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">1</view>
                            <view class="txt">
                                <text>该企业无披露财务数据，注意企业兑付能力与采购能力。点击使用</text>
                                <text @click="toUrl()" class="link" hover-class="none">企业信用报告</text>
                                <text>获取更多内容。</text>
                            </view>
                        </view>
                        <view class="box row verCenter">
                            <view class="num row rowCenter verCenter">2</view>
                            <view class="txt">该企业为小（微）企业，注意企业兑付能力与采购能力</view>
                        </view>
                    </view>
                </view>
            </view>
        </template>
        <!-- 关联企业（47关联企业） -->
        <view class="title row rowCenter verCenter" style="width: 290rpx;">关联企业</view>
        <view v-if="type == 2">
            <view class="relation-sb">
                <view class="relation-bg">
                    <navigator class="bg" style="top: 31rpx;right: 37rpx;" url="/pages/user/login" hover-class="none"></navigator>
                </view>
            </view>
        </view>
        <view class="relation" v-if="type == 1">
            <view class="wrap">
                <view class="bar row">
                    <text class="t1">母公司名称</text>
                    <text class="t2">Sample first</text>
                </view>
                <view class="bar row">
                    <text class="t1">母公司地址</text>
                    <text class="t2">Address Address Address</text>
                </view>
            </view>
        </view>
        <view class="relation" v-if="type == 3">
            <view class="wrap">
                <view class="bar row">
                    <text class="t1">母公司名称</text>
                    <text class="t2">-</text>
                </view>
                <view class="bar row">
                    <text class="t1">母公司地址</text>
                    <text class="t2">-</text>
                </view>
            </view>
        </view>
        <view class="relation" v-if="type == 4">
            <view class="wrap">
                <view class="bar row">
                    <text class="t1">母公司名称</text>
                    <text class="t2">Alphabet Inc.</text>
                </view>
                <view class="bar row">
                    <text class="t1">母公司地址</text>
                    <text class="t2"> Mountain View, CA USA,Unite States</text>
                </view>
            </view>
        </view>
        <!-- 管理层（2管理层） -->
        <view class="title row rowCenter verCenter" style="width: 235rpx;">管理层</view>
        <template v-if="type == 2">
            <view class="management-sb">
                <view class="management-bg">
                    <navigator class="bg" style="top: 35rpx;right: 37rpx;" url="/pages/user/login" hover-class="none"></navigator>
                </view>
            </view>
        </template>
        <template v-if="type == 1">
            <view class="management ">
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">Peter</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">Male</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">President</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">Marry</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">Female</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">President</text>
                    </view>
                </view>
            </view>
        </template>
        <template v-if="type == 3">
            <view class="management ">
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">TIMOTHY D COOK</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">CEO+</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">ARTHUR D LEVINSON</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">CHB+</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">JEFF WILLIAMS</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">COO</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">Al Gore</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">Director</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">LUCA MAESTRI</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">SR V PRES-CFO</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">R123</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">President</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">DEIRDRE O'BRIEN</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">SR V PRES</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">R123</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">President</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">KATE ADAMS</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">SR V PRES-GENERAL COUNSEL-SEC</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">James Bel</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">Director</text>
                    </view>
                </view>
            </view>
            <view class="wrap">
                <view class="box1 row box">
                    <text class="t1 row verCenter">全名</text>
                    <text class="t2 row verCenter">Andrea Jung</text>
                </view>
                <view class="box2 row box">
                    <text class="t1 row verCenter">性别</text>
                    <text class="t2 row verCenter">-</text>
                    <text class="t1 row verCenter">岗位</text>
                    <text class="t2 row verCenter">Director</text>
                </view>
            </view>
            <view class="wrap">
                <view class="box1 row box">
                    <text class="t1 row verCenter">全名</text>
                    <text class="t2 row verCenter">R123</text>
                </view>
                <view class="box2 row box">
                    <text class="t1 row verCenter">性别</text>
                    <text class="t2 row verCenter">-</text>
                    <text class="t1 row verCenter">岗位</text>
                    <text class="t2 row verCenter">President</text>
                </view>
            </view>
            <view class="wrap">
                <view class="box1 row box">
                    <text class="t1 row verCenter">全名</text>
                    <text class="t2 row verCenter">Ronald D Sugar</text>
                </view>
                <view class="box2 row box">
                    <text class="t1 row verCenter">性别</text>
                    <text class="t2 row verCenter">-</text>
                    <text class="t1 row verCenter">岗位</text>
                    <text class="t2 row verCenter">Director</text>
                </view>
            </view>
            <view class="wrap">
                <view class="box1 row box">
                    <text class="t1 row verCenter">全名</text>
                    <text class="t2 row verCenter">Susan L Wagner</text>
                </view>
                <view class="box2 row box">
                    <text class="t1 row verCenter">性别</text>
                    <text class="t2 row verCenter">-</text>
                    <text class="t1 row verCenter">岗位</text>
                    <text class="t2 row verCenter">Director</text>
                </view>
            </view>
        </template>
        <template v-if="type == 4">
            <view class="management ">
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">THOMAS KURIAN</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">CEO</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">RUTH PORAT</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">SR V PRES-CFO</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">DAVID DRUMMOND</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">SR V PRES</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">NIKESH ARORA</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">SR V PRES-CBO</text>
                    </view>
                </view>
                <view class="wrap">
                    <view class="box1 row box">
                        <text class="t1 row verCenter">全名</text>
                        <text class="t2 row verCenter">JADE RAYMOND</text>
                    </view>
                    <view class="box2 row box">
                        <text class="t1 row verCenter">性别</text>
                        <text class="t2 row verCenter">-</text>
                        <text class="t1 row verCenter">岗位</text>
                        <text class="t2 row verCenter">VPRES</text>
                    </view>
                </view>
            </view>
        </template>
        <navigator class="statement" url="/pages/user/agreement" hover-class="none">
            <text class="iconfont iconjinggao"></text>
            <text class="t1">《免责声明》</text>
        </navigator>
        <!-- 更多维度 -->
        <view class="title row rowCenter verCenter" style="width: 143rpx;">更多维度</view>
        <navigator class="more" url="/pages/user/buy" hover-class="none">
            <view class="t1">
                使用
                <text>企业信用报告</text>
                获取更多信息。
            </view>
            <image src="../../static/p3.png" mode="aspectFill" class="im"></image>
        </navigator>
        <view class="login-bar row verCenter" @click="register()" v-if="type == 2">
            <view class="btn row verCenter rowCenter">注册 / 登录</view>
            <text class="txt">免费注册获取更多企业信息。</text>
        </view>
    </view>
</template>

<script>
  import {
    API
  } from '@/util/api.js';

  export default {
    data() {
      return {
        type: 1
      };
    },
    onLoad(options) {
      this.type = options.type;
    },
    onShow() {
    },
    methods: {
      toUrl() {
        uni.navigateTo({
          url: "/pages/user/buy"
        })
      },
      register() {
        uni.showModal({
          title: '',
          content: '绑定账号，立享更多会员权益！',
          cancelText: '放弃',
          confirmText: '免费注册',
          confirmColor: '#0088DD',
          cancelColor: '#999999',
          success: function (res) {
            if (res.confirm) {
              uni.navigateTo({
                url: '/pages/user/login'
              })
            } else if (res.cancel) {
              console.log('用户点击取消');
            }
          }
        });
      },
      wxLogin() {
        uni.login({
          provider: 'weixin',
          success: loginRes => {
            // 获取用户信息
            uni.getUserInfo({
              provider: 'weixin',
              success: infoRes => {
                uni.showToast({
                  title: '授权成功'
                });
              },
              fail: () => {
                uni.showToast({
                  title: '授权失败',
                  icon: 'none'
                });
              }
            });
          },
          fail: () => {
            uni.showToast({
              title: '授权失败',
              icon: 'none'
            });
          }
        });
      }
    }
  };

</script>

<style scoped lang="scss">
    @import '../../assets/css/detail/index.scss';
</style>
