<template lang="html">
  <div class="display_main">
    <div class="head">
      <div class="head_name">
        <span>マイコース</span>
      </div>
      <div class="head_img">
        <img src="../assets/img/リボン.png" alt="">
      </div>
    </div>
    <div class="explanation">
      <subexplanation></subexplanation>
    </div>
    <div class="detail_main">
      <detailmain></detailmain>
    </div>
    </div>
</template>

<script>
    // import subhead from './head/subhead.vue'
    import subexplanation from './explanation/sub_explanation.vue'
    import detailmain from './details/details_main.vue'
    export default {
      components: {
        // subhead,
        subexplanation,
        detailmain
      }
    }
</script>

<style lang="css" scoped>
      /* @import ".src/assets/CSS/web-display-main.css" */
      .display_main{
        width: 100%;
        height:100%;
        margin: auto;
        /* text-align: center; */
      }

      .display_main .head{
        width: 700px;
        height: 70px;
        margin: auto;
        text-align: center;
        position: relative;
      }
      
      .display_main .head .head_name{
        position: absolute;
        top: 17px;
        left: 250px;
        /* フォント設定*/
        text-align: center;
        font-family: "Yu Gothic Medium", "游ゴシック Medium", YuGothic,
          "游ゴシック体", "ヒラギノ角ゴ Pro W3", "メイリオ", sans-serif;
        color: #333333;
        font-size: 35px;
        font-weight: bold;
        text-shadow: 5px 5px 1px #999999;
      }

      .display_main .head .head_img{
        width: 600px;
        height: 70px;
        max-height: 70px;
        margin: auto;
        text-align: center;
      }
      .display_main .head .head_img img{
        width: 100%;
        height: 100%;
        margin: auto;
        text-align: center;
      }

      .display_main .explanation{
        margin-top: 6px;
      }
</style>