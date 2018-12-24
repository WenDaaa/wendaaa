<template>
    <div id="lrb">
        <div class="title">利润表</div>
        <div class="title1">
            <span>编制单位:浙江XXXX科技有限公司</span>
            <span class="timemoney">
                <span>2018年11月</span>
                <span>单位：元</span>
            </span>
        </div>
        <div>
            <table>
                <tr>
                    <th>项目</th>
                    <th>行次</th>
                    <th>本年累计金额</th>
                    <th>本月金额</th>
                </tr>
                <tr>
                    <td>一、营业收入</td>
                    <td>1</td>
                    <td><el-input v-model="Form.YYSR_BNLJJE" placeholder="请输入本年累计金额" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YYSR_SNJE" placeholder="请输入上期金额" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">减：营业成本</td>
                    <td>2</td>
                    <td><el-input v-model="Form.YYCB_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YYCB_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">税金及附加</td>
                    <td>3</td>
                    <td><el-input v-model="Form.YYSJJFJ_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YYSJJFJ_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">其中：消费税</td>
                    <td>4</td>
                    <td><el-input v-model="Form.XFS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.XFS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">营业税</td>
                    <td>5</td>
                    <td><el-input v-model="Form.YYS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YYS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">城市维护建设税</td>
                    <td>6</td>
                    <td><el-input v-model="Form.CSWHJSS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.CSWHJSS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">资源税</td>
                    <td>7</td>
                    <td><el-input v-model="Form.ZYS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.ZYS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">土地增值税</td>
                    <td>8</td>
                    <td><el-input v-model="Form.TDZZS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.TDZZS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">城镇土地使用税、房产税、车船税、印花税</td>
                    <td>9</td>
                    <td><el-input v-model="Form.CZTDSYSYHS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.CZTDSYSYHS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">教育费附加、矿产资源补偿费、排污费</td>
                    <td>10</td>
                    <td><el-input v-model="Form.JYFJPWF_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.JYFJPWF_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">销售费用</td>
                    <td>11</td>
                    <td><el-input v-model="Form.XSYF_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.XSYF_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">其中：商品维修费</td>
                    <td>12</td>
                    <td><el-input v-model="Form.SPWXF_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.SPWXF_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">广告费和业务宣传费</td>
                    <td>13</td>
                    <td><el-input v-model="Form.GGFHYWXCF_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.GGFHYWXCF_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">管理费用</td>
                    <td>14</td>
                    <td><el-input v-model="Form.GLFY_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.GLFY_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">其中：开办费</td>
                    <td>15</td>
                    <td><el-input v-model="Form.KBF_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.KBF_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">业务招待费</td>
                    <td>16</td>
                    <td><el-input v-model="Form.YWZDF_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YWZDF_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">研究费用</td>
                    <td>17</td>
                    <td><el-input v-model="Form.YJFY_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YJFY_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">财务费用</td>
                    <td>18</td>
                    <td><el-input v-model="Form.CWFY_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.CWFY_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">其中：利息费用（收入以'-'号填列）</td>
                    <td>19</td>
                    <td><el-input v-model="Form.LXFY_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.LXFY_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">加：投资收益（损失以'-'号填列）</td>
                    <td>20</td>
                    <td><el-input v-model="Form.TZSY_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.TZSY_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td>二、营业利润(亏损以“-”号填列)</td>
                    <td>21</td>
                    <td><el-input v-model="Form.YYLR_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YYLR_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">加：营业外收入</td>
                    <td>22</td>
                    <td><el-input v-model="Form.YYWSR_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YYWSR_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">其中：政府补助 </td>
                    <td>23</td>
                    <td><el-input v-model="Form.ZFBZ_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.ZFBZ_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">减：营业外支出</td>
                    <td>24</td>
                    <td><el-input v-model="Form.YYWZC_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.YYWZC_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">其中：坏账损失</td>
                    <td>25</td>
                    <td><el-input v-model="Form.HZSS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.HZSS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">无法收回的长期债券投资损失</td>
                    <td>26</td>
                    <td><el-input v-model="Form.WFSHDCQZQTZSS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.WFSHDCQZQTZSS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">无法收回的长期股权投资损失</td>
                    <td>27</td>
                    <td><el-input v-model="Form.WFSHDCQGQTZSS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.WFSHDCQGQTZSS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">自然灾害等不可抗力因素造成的损失</td>
                    <td>28</td>
                    <td><el-input v-model="Form.ZRZHDBKKLYSZCDSS_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.ZRZHDBKKLYSZCDSS_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">税收滞纳金</td>
                    <td>29</td>
                    <td><el-input v-model="Form.SSZNJ_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.SSZNJ_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td>三、利润总额(亏损总额以“-”号填列)</td>
                    <td>30</td>
                    <td><el-input v-model="Form.LRZE_BNLJJE" placeholder="请输入本年累计金额"value="0.00" class="a"></el-input> </td>
                    <td><el-input v-model="Form.LRZE_SNJE" placeholder="请输入上期金额"value="0.00" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td class="p-right">减：所得税费用</td>
                    <td>31</td>
                    <td><el-input v-model="Form.SDSFY_BNLJJE" placeholder="请输入本年累计金额" class="a"></el-input> </td>
                    <td><el-input v-model="Form.SDSFY_SNJE" placeholder="请输入上期金额" class="a"></el-input> </td>
                </tr>
                <tr>
                    <td>四、净利润(净亏损以“-”号填列)</td>
                    <td>32</td>
                    <td><el-input v-model="Form.JLR_BNLJJE" placeholder="请输入本年累计金额" class="a"></el-input> </td>
                    <td><el-input v-model="Form.JLR_SNJE" placeholder="请输入上期金额" class="a"></el-input> </td>
                </tr>
            </table>
            <div>{{Form}}</div>
            <el-button type="success" @click="pushlrb" class="bth">提交利润表</el-button>
        </div>
    
    </div>
</template>
<script>

export default {
    data:function(){
        return{
            Form:{ }
        }
    },
    methods:{
        pushlrb(){
            console.log(this.Form.JLR_SNJE,this.Form.JLR_BNLJJE)
        },
        checknum(e){




            // console.log(e)
            // var reg = /^(-?[1-9]\d{0,5}\.\d{1,2}|-?0\.\d{1,2}|-?[1-9]\d{0,5}|0)/;
            //     if(reg.test(e.target.value)){
            //         e.srcElement.value = e.target.value.match(reg)[0]
            //     }else{
            //         e.srcElement._value = '0.00'
            //     }
        }

    }
}
</script>
<style scoped>
    .p-right{
        padding-left: 30px;
    }
    .table>tr>td:nth-child(1){
        padding:0px 17px;
    }
    .a{
        width: 200px;
    }
    table>tr>td:nth-child(1){
        width: 50%
    }
    table>tr>th:nth-child(1){
        width: 10%
    }
    table>tr>td:nth-child(2){
        width: 10%
    }
    table>tr>th:nth-child(2){
        width: 10%
    }
    table{
        border: 1px solid #ddd;
        border-collapse: collapse;
    }
    th{
        border: 1px solid #ddd;
    }
    td{
        border:1px solid #ddd;
    }
    .title{
        text-align: center;
        font-size: 23px;
        font-weight: 500;
    }
    .title1{
        display: flex;
        justify-content: space-between;
    }
    .timemoney>span{
        display: inline-block;
        width: 150px;
    }
    #lrb{
        width: 100%;
        min-width: 800px;
    }
    *{
        color: #333;
    }
</style>