<template>
    <div class="details_main row">
            <div class="col-lg-98">
                <div class="details_item">
                    <item></item>
                </div>
            </div>
            <div class="col-lg-3">
                <div class="details_other">
                    <div class="map">
                        <img src="../../assets/img/map.png" alt="">
                    </div>
                    <div class="position">
                        <span>ここは位置</span> 
                        <positiontable></positiontable>
                    </div>
                    <div class="knowledge">
                        <span>ここは豆知識</span> 
                    </div>
                    <div class="recommend">
                        <span>その他</span>
                        <div class="recommend-item">
                            <draggable>
                                <div class="recommend-img" v-for="item in items" :key="item.id">
                                    <img :src="item.url" alt="">
                                </div>
                            </draggable>
                        </div>
                    </div>
                </div>
            </div>
        </div>
</template>

<script>
    import item from "./item.vue"
    import positiontable from "./position_table.vue"
    import draggable from 'vuedraggable'

    export default {
      components: {
        item,
        positiontable,
        draggable,
      },
      data(){
        return{  
            items: [
                {id:1, name: 'name1', text: 'test1', url: require('../../assets/img/ex_3.jpg')},
                {id:2, name: 'name2', text: 'test2', url: require('../../assets/img/ex_3.jpg')},
                {id:3, name: 'name3', text: 'test3', url: require('../../assets/img/ex_13.jpg')},
                {id:4, name: 'name4', text: 'test4', url: require('../../assets/img/ex_1.jpg')},
                {id:5, name: 'name5', text: 'test5', url: require('../../assets/img/ex_11.jpg')},
                ]
            }
        }
    }
</script>

<style lang="css" scoped> 
    .details_main{
        width: 1200px;
        height: 740px;
        margin: auto;
    }

    .details_main .details_item{
        width: 850px;
        height: 725px;
        margin: auto;
    }

    .details_main .details_other{
        width: 310px;
        height: 725px;
        margin: auto;
        margin-top: 5px;
    }

    .details_main .details_other .map{
        width: 310px;
        height: 310px;
        margin: auto;
    }
    .details_main .details_other .map img{
        width: 100%;
        height: 100%;
    }

    .details_main .details_other .position{
        width: 320px;
        height: 100px;
        margin-top: 2px;
        border-radius: 10px;
        border: rgb(160, 211, 22) solid 2px;
        background: rgb(160, 211, 22);
    }

    .details_main .details_other .knowledge{
        width: 320px;
        height: 140px;
        margin-top: 8px;
        border-radius: 10px;
        border: rgb(160, 211, 22) solid 2px;
        background: rgb(160, 211, 22);
    }

    .details_main .details_other .recommend{
        width: 320px;
        height: 130px;
        margin: auto;
        margin-top: 6px;
        border-radius: 10px;
        border: rgb(160, 211, 22) solid 2px;
        background: rgb(160, 211, 22);
    }

    .details_main .details_other .recommend .recommend-item{
        margin: auto;
        margin-top: 10px;
        display: flex;
    }
    .details_main .details_other .recommend .recommend-item .recommend-img{
        width: 60px;
        height: 60px;
        margin: auto;
        display: inline-block;
        margin-left: 2px;
    }

    .details_main .details_other .recommend .recommend-item img{
        width: 100%;
        height: 100%;
    }
</style>