<template>
  <div class="components-container">
    <code>drag-list base on
      <a href="https://github.com/SortableJS/Vue.Draggable" target="_blank">Vue.Draggable</a>
    </code>
    <div class="editor-container">
      <dnd-list :list1="list1" :list2="list2" list1-title="List" list2-title="Article pool"/>
    </div>
  </div>
</template>

<script>
import DndList from '../components/DndList'
// import { fetchList } from '@/api/article'

export default {
  name: 'DndListDemo',
  components: { DndList },
  data() {
    return {
      list1: [],
	  list2: [],
	  list:[{"id":7,"timestamp":1328361256180,"author":"Larry","reviewer":"Richard","title":"Bvvq Rlqvdq Qbebygewof Feybdt Empyc Orwqhwo","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":17.74,"importance":2,"type":"US","status":"deleted","display_time":"2005-06-21 23:17:33","comment_disabled":true,"pageviews":2343,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":8,"timestamp":587379239342,"author":"Brian","reviewer":"Edward","title":"Lsudaqlbxo Npxsj Tgyextj Gnzu Igemhpc Jxrflwe Eunryip Jtmoqkk","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":14.44,"importance":2,"type":"US","status":"published","display_time":"1975-01-26 09:05:13","comment_disabled":true,"pageviews":2200,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":5,"timestamp":1014882564793,"author":"Carol","reviewer":"Daniel","title":"Wumohqo Fmmckivn Orgedxq Geknspy Ygoecyd Tfhbmcdp Rlspnczji","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":21.68,"importance":3,"type":"US","status":"draft","display_time":"1990-07-21 19:28:29","comment_disabled":true,"pageviews":1611,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":4,"timestamp":561482841558,"author":"Thomas","reviewer":"Margaret","title":"Qtyfefwqf Nfnlp Yoz Qhzzomnq Yefrq Zxutk Khfhx","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":60.06,"importance":1,"type":"EU","status":"draft","display_time":"1998-05-03 02:53:16","comment_disabled":true,"pageviews":399,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":3,"timestamp":1391384177361,"author":"Helen","reviewer":"Mary","title":"Hcefjnxg Seenln Evghyghv Dmwudwkrvl Hhcil Ekcqqi Phatckx Xcchfkyuhr","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":89.47,"importance":2,"type":"US","status":"deleted","display_time":"1982-08-29 06:38:50","comment_disabled":true,"pageviews":4927,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":2,"timestamp":247389451870,"author":"Elizabeth","reviewer":"Anna","title":"Wmlgyv Coymtbmg Fmekyvsn Mcmhupdx Gujrcj Bvoxqvp Sctbgqhcp Jleagy Ncwhovljw","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":65.17,"importance":1,"type":"US","status":"deleted","display_time":"2014-07-24 12:37:50","comment_disabled":true,"pageviews":1046,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":6,"timestamp":767529018441,"author":"Shirley","reviewer":"Dorothy","title":"Rpf Xgxtvypou Ohxyso Ipbex Lesvdxusd Sbtuszetgi Gyng Iuesdk","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":95.64,"importance":2,"type":"US","status":"draft","display_time":"1994-06-17 15:44:27","comment_disabled":true,"pageviews":1060,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":1,"timestamp":26231941398,"author":"Larry","reviewer":"Donna","title":"Cxsgxk Dkoidzhwy Heksqu Nmlkip Etdcr","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":78.38,"importance":3,"type":"US","status":"published","display_time":"1996-10-10 22:50:38","comment_disabled":true,"pageviews":4349,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":9,"timestamp":1049188520959,"author":"Steven","reviewer":"Timothy","title":"Lrxsw Manwztwkn Lnuvovn Skbso Otftwhuwx Bypxidch Pgfen Fdahxm","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":64.03,"importance":2,"type":"JP","status":"draft","display_time":"2016-01-17 22:49:20","comment_disabled":true,"pageviews":802,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]},{"id":10,"timestamp":84205715700,"author":"Kevin","reviewer":"Melissa","title":"Vhyrh Mmyzrdrqst Wtf Jwvvwkppbr Ueieexyus Kfjpo Bmtoh","content_short":"我是测试数据","content":"<p>我是测试数据我是测试数据</p><p><img src=\"https://wpimg.wallstcn.com/4c69009c-0fd4-4153-b112-6cb53d1cf943\"></p>","forecast":48.36,"importance":3,"type":"CN","status":"deleted","display_time":"1980-07-09 17:45:48","comment_disabled":true,"pageviews":2541,"image_uri":"https://wpimg.wallstcn.com/e4558086-631c-425c-9430-56ffb46e70b3","platforms":["a-platform"]}]
    }
  },
  created() {
    this.getData()
  },
  methods: {
    getData() {
      this.listLoading = true
     
        this.list1 = this.list.splice(0, 5)
        this.list2 = this.list
   
    }
  }
}
</script>

