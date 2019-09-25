<template>
    <div>
        <div class="explanation">
            <div class="explanation_name">
                <span>アイテム--</span>
            </div>
            <div class="explanation_item">
                <span>釣り</span>
            </div>
            <div class="explanation_content">
                <span>魚を収穫する為、重要な道具であり、釣り針は何千年も前に発明されたと考えられる。工夫した釣針はどんな特徴があるでしょう。
                    魚を収穫する為、重要な道具であり、釣り針は何千年も前に発明されたと考えられる。工夫した釣針はどんな特徴があるでしょう。</span>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style type="CSS" scoped>
    .explanation{
        width: 1100px;
        height: 60px;
        margin-top: 3px;
        margin: auto;
        display: flex;
        text-align: center;
        border-radius: 10px;
        border: #FFFFAA solid 2px;
        background: #FFFFAA;
    }

    .explanation_name{
        width: 20%;
        height: 100%;
        text-align: center;
        font-family: "Yu Gothic Medium", "游ゴシック Medium", YuGothic,
          "游ゴシック体", "ヒラギノ角ゴ Pro W3", "メイリオ", sans-serif;
        color: #333333;
        font-size: 35px;
        font-weight: bold;
        /* text-shadow: 5px 5px 1px #999999; */
    }
    .explanation_item{
        width: 15%;
        height: 100%;
        text-align: left;
        font-family: "Yu Gothic Medium", "游ゴシック Medium", YuGothic,
          "游ゴシック体", "ヒラギノ角ゴ Pro W3", "メイリオ", sans-serif;
        color: #333333;
        font-size: 35px;
        font-weight: bold;

    }
    .explanation_content{
        width: 65%;
        height: 100%;
        max-width: 65%;
        max-height: 100%;
        text-align: left;
        font-family: "Yu Gothic Medium", "游ゴシック Medium", YuGothic,
          "游ゴシック体", "ヒラギノ角ゴ Pro W3", "メイリオ", sans-serif;
        color: #333333;
        font-size: 15px;
        font-weight: bold;
    }

    .explanation_content .span{
        max-width: 100%;
        max-height: 100%;
    }
</style>