<template>
    <div class="position_table">
        <table class="basic-table">
            <thead>
                <tr>
                    <th>1</th>
                    <th>2</th>
                    <th>3</th>
                    <th>4</th>
                    <th>5</th>
                    <th>6</th>
                    <th>7</th>
                    <th>8</th>
                    <th>9</th>
                    <th>10</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>E5</td>
                    <td>E5</td>
                    <td>E5</td>
                    <td>E5</td>
                    <td>E6</td>
                    <td>E10</td>
                    <td>E12</td>
                    <td>D5</td>
                    <td>F5</td>
                    <td>E5</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
</script>

<style lang="css" scoped>
    .position_table .basic-table{
        margin: auto;
        text-align: center;
        /* フォント設定*/
        font-family: "Yu Gothic Medium", "游ゴシック Medium", YuGothic,
          "游ゴシック体", "ヒラギノ角ゴ Pro W3", "メイリオ", sans-serif;
        color: #333333;
        font-size: 15px;
        font-weight: bold;
    }

    .position_table .basic-table{
        border-collapse: collapse;
    }

    .position_table .basic-table th {
        border: solid 2px; 
    }

    .position_table .basic-table td {
        border: solid 2px;
        padding: 0.3em;
    }
</style>