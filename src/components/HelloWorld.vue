<template>
  <div class="hello">
    <button onclick="export()">导出</button>
  </div>
</template>

<script >
const ExportJsonExcel = require('js-export-excel');
window.onload = function() {
  console.log(window);
  var option = {};
  option.fileName = "excel";
  option.datas = [
    {
      sheetData: [
        { one: "一行一列", two: "一行二列" },
        { one: "二行一列", two: "二行二列" }
      ],
      sheetName: "sheet",
      sheetFilter: ["two", "one"],
      sheetHeader: ["第一列", "第二列"]
    },
    {
      sheetData: [
        { one: "一行一列", two: "一行二列" },
        { one: "二行一列", two: "二行二列" }
      ]
    }
  ];
  // var toExcel = new ExportJsonExcel(option);
  // toExcel.saveExcel();
};
// import ExportJsonExcel from 'ExportJsonExcel'
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  },
  methods: {
    //     export(){
    //       console.log('sdfsfd');
    //       var option={};
    // option.fileName = 'excel'
    // option.datas=[
    //   {
    //     sheetData:[{one:'一行一列',two:'一行二列'},{one:'二行一列',two:'二行二列'}],
    //     sheetName:'sheet',
    //     sheetFilter:['two','one'],
    //     sheetHeader:['第一列','第二列']
    //   },
    //   {
    //     sheetData:[{one:'一行一列',two:'一行二列'},{one:'二行一列',two:'二行二列'}]
    //   }
    // ];
    // var toExcel=new ExportJsonExcel(option);
    // toExcel.saveExcel();
    //     }
  },
  created() {
    // this.export()
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
