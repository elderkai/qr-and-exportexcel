<template>
  <div>
    <h1>qr</h1>
    <p><a href="https://github.com/Binaryify/vue-qr">查看github帮助</a></p>
      <!-- :autoColor="true"  若为 true, 背景图的主要颜色将作为实点的颜色, 即 colorDark-->
<!-- backgroundDimming='red'叠加在背景图上的颜色, 在解码有难度的时有一定帮助 -->
<!--       colorLight='#111'空白区的颜色  -->
<!-- :whiteMargin='true' , 背景图外将绘制白色边框 -->
<!-- binarize=true 若为 true, 图像将被二值化处理, 未指定阈值则使用默认值 -->
<!-- colorDark 实点的颜色 -->
      <!-- :logoSrc="src2" -->
    <vue-qr
      :bgSrc="src3"
      colorDark="#1E82C0"
      autoColor='true'
      dotScale='0.5'
      text="Helloewfewwwwdsddddd world!"
      :size="200"
    ></vue-qr>
    <!-- <vue-qr text="Hello world!" :callback="test" qid="testid"></vue-qr> -->
  </div>
</template>

<script>
import VueQr from "vue-qr";
export default {
  components: { VueQr },
  data() {
    return {
      true:true,
      src:
        "https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=2516869015,3471694557&fm=58",
      src2:
        "https://ss1.baidu.com/6ONXsjip0QIZ8tyhnq/it/u=2516869015,3471694557&fm=58",
        src3:
        "https://ss0.baidu.com/6ONWsjip0QIZ8tyhnq/it/u=1211395833,2279143731&fm=58"
    };
  },
  methods: {
    test(dataUrl, id) {}
  }
};
</script>

<style scoped>
</style>
