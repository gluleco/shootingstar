
## 数据表描述
<style type="text/css">
.tg  {border-collapse:collapse;border-color:#93a1a1;border-spacing:0;margin:0px auto;}
.tg td{background-color:#fdf6e3;border-color:#93a1a1;border-style:solid;border-width:1px;color:#002b36;
  font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{background-color:#657b83;border-color:#93a1a1;border-style:solid;border-width:1px;color:#fdf6e3;
  font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-lboi{border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-9wq8{border-color:inherit;text-align:center;vertical-align:middle}
.tg .tg-00qb{border-color:inherit;position:-webkit-sticky;position:sticky;text-align:center;top:-1px;vertical-align:middle;
  will-change:transform}
@media screen and (max-width: 767px) {.tg {width: auto !important;}.tg col {width: auto !important;}.tg-wrap {overflow-x: auto;-webkit-overflow-scrolling: touch;margin: auto 0px;}}</style>
<div class="tg-wrap"><table class="tg" style="undefined;table-layout: fixed; width: 939px"><colgroup>
<col style="width: 123.047619px">
<col style="width: 330.047619px">
<col style="width: 183.047619px">
<col style="width: 303.047619px">
</colgroup>
<thead>
  <tr>
    <th class="tg-00qb">功能模块</th>
    <th class="tg-00qb">Resource</th>
    <th class="tg-00qb">Symbol</th>
    <th class="tg-00qb">简要说明</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-9wq8" rowspan="5">股指期货年化基差</td>
    <td class="tg-9wq8" rowspan="5">anti.RiskControl.IndexFutureBasis</td>
    <td class="tg-9wq8">期货简称_currentquarter</td>
    <td class="tg-lboi" rowspan="4">主要包括四个股指期货IH（上证50）、IF（沪深300）、IC（中证500）、IM（中证1000）的当季和次季、当月和次月合约上市以来基差率以及年化基差数据。近期合约成交比较活跃，但到期日比较短，年化基差计算误差相对比较大；远期合约成交相对不活跃，但到期时间相对比较长，年化基差计算误差相对比较小。</td>
  </tr>
  <tr>
    <td class="tg-9wq8">期货简称_nextquarter</td>
  </tr>
  <tr>
    <td class="tg-9wq8">期货简称_currentmonth</td>
  </tr>
  <tr>
    <td class="tg-9wq8">期货简称_nextmonth</td>
  </tr>
  <tr>
    <td class="tg-9wq8">BasisChange</td>
    <td class="tg-lboi">包含各个合约的上市以来每日基差的变化率，扩张or收敛。</td>
  </tr>
  <tr>
    <td class="tg-9wq8" rowspan="3">北向资金数据</td>
    <td class="tg-9wq8" rowspan="3">anti.RiskControl.MarketEnvironment:CapitalFlows</td>
    <td class="tg-9wq8">north-capital-MHN</td>
    <td class="tg-lboi">整体</td>
  </tr>
  <tr>
    <td class="tg-9wq8">north-capital-SZN</td>
    <td class="tg-lboi">沪市</td>
  </tr>
  <tr>
    <td class="tg-9wq8">north-capital-SHN</td>
    <td class="tg-lboi">深市</td>
  </tr>
  <tr>
    <td class="tg-9wq8" rowspan="3">流动性风险相关</td>
    <td class="tg-9wq8">anti.RiskControl.StkADV</td>
    <td class="tg-9wq8">stock_ADTV_data</td>
    <td class="tg-lboi">计算每日A股的不同期限的trading volume</td>
  </tr>
  <tr>
    <td class="tg-9wq8">anti.RiskControl.ProductDailyHold:ADVratio</td>
    <td class="tg-9wq8">adtv_ratio_wholecompany</td>
    <td class="tg-lboi">计算整个公司持有的每只股票的adv变现比例（假设在1天之内卖出）</td>
  </tr>
  <tr>
    <td class="tg-9wq8">anti.RiskControl.ProductDailyHold:ADVratio</td>
    <td class="tg-9wq8">product_ADVratio_top10</td>
    <td class="tg-lboi">计算每个产品持有的股票的adv变现比例Top 10（假设在1天之内卖出）</td>
  </tr>
</tbody></table></div>

## 数据表列表  
<style type="text/css">
.tg  {border-collapse:collapse;border-color:#93a1a1;border-spacing:0;margin:0px auto;}
.tg td{background-color:#fdf6e3;border-color:#93a1a1;border-style:solid;border-width:1px;color:#002b36;
  font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{background-color:#657b83;border-color:#93a1a1;border-style:solid;border-width:1px;color:#fdf6e3;
  font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-icfc{color:#ffffff;position:-webkit-sticky;position:sticky;text-align:center;top:-1px;vertical-align:middle;
  will-change:transform}
@media screen and (max-width: 767px) {.tg {width: auto !important;}.tg col {width: auto !important;}.tg-wrap {overflow-x: auto;-webkit-overflow-scrolling: touch;margin: auto 0px;}}</style>
<div class="tg-wrap"><table class="tg"><thead>
  <tr>
    <th class="tg-icfc">QueryTableList</th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.IndexFutureBasis', symbol='IC_currentquarter',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.IndexFutureBasis', symbol='IC_nextquarter',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.IndexFutureBasis', symbol='IC_currentmonth',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.IndexFutureBasis', symbol='IC_nextmonth',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.IndexFutureBasis', symbol='BasisChange',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.MarketEnvironment:CapitalFlows', symbol='north-capital-MHN',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.MarketEnvironment:CapitalFlows', symbol='north-capital-SZN',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.MarketEnvironment:CapitalFlows', symbol='north-capital-SHN',date_range=["20240101","20240304"])  </td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.StkADV', '"+date+".stock_ADTV_data')</td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.ProductDailyHold:ADVratio', symbol=""+date+".product_ADVratio_top10")</td>
  </tr>
  <tr>
    <td class="tg-cly1">WQData.query_data('anti.RiskControl.ProductDailyHold:ADVratio', symbol=""+date+".adtv_ratio_wholecompany")</td>
  </tr>
</tbody></table></div>