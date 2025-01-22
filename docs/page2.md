## 数据表使用  


* 登录API接口  

    `from WQOneData import WQData`  
    `WQData.login(ldap_username,ldap_password)` # ldap账号密码即登录官网的账号密码  

* 元数据格式为 `{source}.{database}.{resource}`，目前写入数据库为ANTI，resource下有多个symbol表进行查询  
* 列出resource下的所有symbol, `WQData.list_symbols(anti.[your_database].[your_resource])`  

* 使用举例  

    选择一段时间进行查询需要指定date_range字段，`date_range=["date1","date2"]`  
                eg: `WQData.query_data('source.database.resource', symbol='X',date_range=["date1","date2"])`


## 数据表描述
<style type="text/css">
.tg  {border-collapse:collapse;border-color:#93a1a1;border-spacing:0;}
.tg td{background-color:#fdf6e3;border-color:#93a1a1;border-style:solid;border-width:1px;color:#002b36;
  font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{background-color:#657b83;border-color:#93a1a1;border-style:solid;border-width:1px;color:#fdf6e3;
  font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-lboi{border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-9wq8{border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-k1tv{border-color:inherit;color:#ffffff;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 1306px"><colgroup>
<col style="width: 115.047619px">
<col style="width: 326.047619px">
<col style="width: 237.047619px">
<col style="width: 628.047619px">
</colgroup>
<thead>
  <tr>
    <th class="tg-k1tv">功能模块</th>
    <th class="tg-k1tv">Resource</th>
    <th class="tg-k1tv">Symbol</th>
    <th class="tg-k1tv">简要说明</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-9wq8" rowspan="5">BARRA因子相关</td>
    <td class="tg-9wq8" rowspan="5">anti.RiskControl.ProductDailyHold:Barra</td>
    <td class="tg-9wq8">BARRA-long</td>
    <td class="tg-lboi">产品barra因子暴露（纯多头）</td>
  </tr>
  <tr>
    <td class="tg-9wq8">BARRA-delta</td>
    <td class="tg-lboi">产品barra因子暴露（多空轧差后）</td>
  </tr>
  <tr>
    <td class="tg-9wq8">BARRA-active</td>
    <td class="tg-lboi">产品barra因子暴露（多空轧差+减去对标基准）</td>
  </tr>
  <tr>
    <td class="tg-nrix">BARRA-facret</td>
    <td class="tg-cly1">产品barra因子收益，计算因子收益使用 T-1日的资产组合因子暴露 * T日的barra因子收益率</td>
  </tr>
  <tr>
    <td class="tg-nrix">BARRA-topratio</td>
    <td class="tg-cly1">产品barra因子占比统计，包括行业因子long-cumsum前10、行业因子long前10、行业因子active前3、风格因子active前3、行业因子active-sum、风格因子active-sum</td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="4">申万行业相关</td>
    <td class="tg-nrix" rowspan="4">anti.RiskControl.ProductDailyHold:SWind</td>
    <td class="tg-nrix">SWind-long</td>
    <td class="tg-cly1">产品申万行业占比（纯多头）</td>
  </tr>
  <tr>
    <td class="tg-nrix">SWind-delta</td>
    <td class="tg-cly1">产品申万行业占比（多空轧差后）</td>
  </tr>
  <tr>
    <td class="tg-nrix">SWind-active</td>
    <td class="tg-cly1">产品申万行业占比（多空轧差+减去对标基准）</td>
  </tr>
  <tr>
    <td class="tg-nrix">SWind-topratio</td>
    <td class="tg-cly1">产品申万行业常用数据速查，行业long-cumsum前10、行业long前10、行业active前3</td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="4">中信行业相关</td>
    <td class="tg-nrix" rowspan="4">anti.RiskControl.ProductDailyHold:CITICSind</td>
    <td class="tg-nrix">CITICSind-long</td>
    <td class="tg-cly1">产品中信行业占比（纯多头）</td>
  </tr>
  <tr>
    <td class="tg-nrix">CITICSind-delta</td>
    <td class="tg-cly1">产品中信行业占比（多空轧差后）</td>
  </tr>
  <tr>
    <td class="tg-nrix">CITICSind-active</td>
    <td class="tg-cly1">产品中信行业占比（多空轧差+减去对标基准）</td>
  </tr>
  <tr>
    <td class="tg-nrix">CITICSind-topratio</td>
    <td class="tg-cly1">产品中信行业常用数据速查，行业long-cumsum前10、行业long前10、行业active前3</td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="5">持仓风格分布</td>
    <td class="tg-nrix" rowspan="5">anti.RiskControl.ProductDailyHold:Splitportfolio</td>
    <td class="tg-nrix">index-and-sector-coverage</td>
    <td class="tg-cly1">产品指数和板块持仓分布</td>
  </tr>
  <tr>
    <td class="tg-nrix">free-marketcap-layer</td>
    <td class="tg-cly1">对持仓组合进行分类分层，选【流通市值】进行比较,采用安信和平安的两分类阈值。安信分类：[40,100,500]，平安分类1：[100,500,1000]，平安分类2：[0.07,0.22]</td>
  </tr>
  <tr>
    <td class="tg-nrix">marketcap-layer</td>
    <td class="tg-cly1">对持仓组合进行分类分层，选【市值】进行比较,采用安信和平安的两种分类阈值。安信分类：[40,100,500]，平安分类1：[100,500,1000]</td>
  </tr>
  <tr>
    <td class="tg-nrix">style-analysis</td>
    <td class="tg-cly1">对持仓组合风格进行网格分类统计，参考晨星风格箱3*3的结构对股票进行分类，分别是大中小市值，成长价值平衡</td>
  </tr>
  <tr>
    <td class="tg-nrix">average-marketcap</td>
    <td class="tg-cly1">对持仓的市值进行统计，按照加权（不加权）* 纯股票（股票+期货拆分）四种算法进行计算</td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="6">持仓集中度</td>
    <td class="tg-nrix" rowspan="6">anti.RiskControl.ProductDailyHold:Concentration</td>
    <td class="tg-nrix">stock-num</td>
    <td class="tg-cly1">持股数量，包含long、short、delta、purestock long and short</td>
  </tr>
  <tr>
    <td class="tg-nrix">top-hold-ratio</td>
    <td class="tg-cly1">个股持仓占比-多头口径（含股指期货）包含个股top-long-cumsum的统计，分母包含longvalue和netasset两种口径下的计算</td>
  </tr>
  <tr>
    <td class="tg-nrix">top-hold-ratio-purestock</td>
    <td class="tg-cly1">个股持仓占比-多头口径（纯股票，不含股指期货）</td>
  </tr>
  <tr>
    <td class="tg-nrix">top-hold-info-long</td>
    <td class="tg-cly1">产品前10持仓占比信息(纯多头)</td>
  </tr>
  <tr>
    <td class="tg-nrix">top-hold-info-delta</td>
    <td class="tg-cly1">产品前10持仓占比信息(多空轧差)</td>
  </tr>
  <tr>
    <td class="tg-nrix">product_decompose_ratio</td>
    <td class="tg-cly1">产品的多头市值占比、敞口比率、各项资产占净资产的比例</td>
  </tr>
  <tr>
    <td class="tg-nrix" rowspan="2">期货持仓价值</td>
    <td class="tg-nrix" rowspan="2">anti.RiskControl.ProductDailyHold:Futureholdvalue</td>
    <td class="tg-nrix">future_value_based_index</td>
    <td class="tg-cly1">股指期货持仓市值（不含CTA），仓位 * benchmark price</td>
  </tr>
  <tr>
    <td class="tg-nrix">future_value_based_settlementprice</td>
    <td class="tg-cly1">股指期货持仓市值（不含CTA），仓位 * settlement price</td>
  </tr>
  <tr>
    <td class="tg-nrix">收益率类</td>
    <td class="tg-nrix">anti.RiskControl.ProductDailyHold:Yieldanalysis</td>
    <td class="tg-nrix">daily-yield-distribution</td>
    <td class="tg-cly1">日收益率分布常用的统计指标，包含历史日收益率（分红调整后计算）max、min、mean、std、skew、kurtosis、median、quantile</td>
  </tr>
  <tr>
    <td class="tg-nrix">主动管理</td>
    <td class="tg-nrix">anti.RiskControl.ProductDailyHold:Activeshare</td>
    <td class="tg-nrix">product-active-share</td>
    <td class="tg-cly1">计算产品的active share，算法是active_share = abs(stock weight - benchmark weight).sum()/2<br>一个完全复制基准的投资组合的Active Share为0%，而一个完全不复制基准的投资组合的Active Share为100%。</td>
  </tr>
  <tr>
    <td class="tg-nrix">事前BETA</td>
    <td class="tg-nrix">anti.RiskControl.ProductDailyHold:Portfoliobeta</td>
    <td class="tg-nrix">beta_basedon_riskmodel</td>
    <td class="tg-cly1">产品跟市场bm过去一年的收益率进行OLS回归的系数，进行了上下限调整0.5-1.2（使用回归方法得到的结果和使用cov(product,market)/var(market)公式的一致）</td>
  </tr>
</tbody></table>

## 数据表列表  

<style type="text/css">
.tg  {border-collapse:collapse;border-color:#93a1a1;border-spacing:0;}
.tg td{background-color:#fdf6e3;border-color:#93a1a1;border-style:solid;border-width:1px;color:#002b36;
  font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{background-color:#657b83;border-color:#93a1a1;border-style:solid;border-width:1px;color:#fdf6e3;
  font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-igm5{background-color:#fff2cc;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-qrc3{background-color:#fff2cc;border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-uzvj{border-color:inherit;font-weight:bold;text-align:center;vertical-align:middle}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 1003px"><colgroup>
<col style="width: 1003.047619px">
</colgroup>
<thead>
  <tr>
    <th class="tg-uzvj">QueryTableList</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:SWind', symbol='SWind-long',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:SWind', symbol='SWind-delta',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:SWind', symbol='SWind-active',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:SWind', symbol='SWind-topratio',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:CITICSind', symbol='CITICSind-long',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:CITICSind', symbol='CITICSind-delta',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:CITICSind', symbol='CITICSind-active',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:CITICSind', symbol='CITICSind-topratio',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Barra', symbol='BARRA-long',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Barra', symbol='BARRA-delta',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Barra', symbol='BARRA-active',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Barra', symbol='BARRA-facret',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Barra', symbol='BARRA-topratio',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Splitportfolio', symbol='index-and-sector-coverage',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Splitportfolio', symbol='free-marketcap-layer',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-qrc3">WQData.query_data('anti.RiskControl.ProductDailyHold:Splitportfolio', symbol='marketcap-layer',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Splitportfolio', symbol='style-analysis',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-qrc3">WQData.query_data('anti.RiskControl.ProductDailyHold:Splitportfolio', symbol='average-marketcap',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Concentration', symbol='stock-num',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Concentration', symbol='top-hold-ratio',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-qrc3">WQData.query_data('anti.RiskControl.ProductDailyHold:Concentration', symbol='top-hold-ratio-purestock',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Concentration', symbol='top-hold-info-long',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Concentration', symbol='top-hold-info-delta',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Concentration', symbol='product_decompose_ratio',date_range=["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Futureholdvalue', symbol='future_value_based_index',date_range=["20240101","20240304"]) </td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Futureholdvalue', symbol='future_value_based_settlementprice',date_range = ["20240101","20240304"])</td>
  </tr>
  <tr>
    <td class="tg-igm5">WQData.query_data('anti.RiskControl.ProductDailyHold:Yieldanalysis', symbol='daily-yield-distribution',date_range=["20240101","20240304"]) </td>
  </tr>
  <tr>
    <td class="tg-qrc3">WQData.query_data('anti.RiskControl.ProductDailyHold:Activeshare', symbol=""+date+".product-active-share")</td>
  </tr>
  <tr>
    <td class="tg-qrc3">WQData.query_data('anti.RiskControl.ProductDailyHold:Portfoliobeta', symbol=""+date+".beta_basedon_riskmodel")</td>
  </tr>
</tbody></table>