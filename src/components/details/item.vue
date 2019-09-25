<template>
    <div class="item">
        <b-card-group deck class="item-group">
            <draggable v-model="itemList" @end="end">
                <b-card class="item-card" v-for="item in itemList" :key="item.id" :img-src="item.url" img-alt="item-img" img-width="160px" img-height="160px" img-top>  
                    <b-card-title title-tag="h5">
                        {{item.name}}
                    </b-card-title>
                    <b-card-text text-tag="span">
                        <ul>
                            <li><a href="#" class="card-link">#{{item.text}}</a></li>
                            <li><a href="#" class="card-link">#{{item.text}}</a></li>
                            <li><a href="#" class="card-link">#{{item.text}}</a></li>
                            <li><a href="#" class="card-link">#{{item.text}}</a></li>
                        </ul> 
                    </b-card-text>     
                    <b-button pill variant="outline-secondary btn-sm" click="Deletecard(item.id, index)">
                        Delete
                    </b-button>                                                                                             
                </b-card>
            </draggable>
        </b-card-group>
    </div>
</template>

<script>
    import draggable from 'vuedraggable'
    // import axios from 'axios'
    import data from '../../assets/data.json'

    export default{
        name: "dnd",
        components: {
            draggable,
        },
        data () {
            return{
                itemList: data,
            }
        },
        mounted () {
            // axios
            //     .get("/static/data.json")
            //     .then(response =>{
            //         window.console.log(response);
            //         this.items = response.data;
            //    })   
        },
        methods:{
            end(){
                this.$eventHub.$emit('change-position', this.itemList);
            }
        },
        // data(){
        //     return{  
        //         itemList: [
        //             {id:1, name: 'name1', text: 'てすとてす', url: require('../../assets/img/ex_3.jpg')},
        //             {id:2, name: 'イラン帝国', text: 'test2', url: require('../../assets/img/ex_11.jpg')},
        //             {id:3, name: 'name3', text: 'test3', url: require('../../assets/img/ex_11.jpg')},
        //             {id:4, name: 'name4', text: 'test4', url: require('../../assets/img/ex_1.jpg')},
        //             {id:5, name: 'name5', text: 'test5', url: require('../../assets/img/ex_13.jpg')},
        //             {id:6, name: 'name6', text: 'test6', url: require('../../assets/img/ex_1.jpg')},
        //             {id:7, name: 'name7', text: 'test7', url: require('../../assets/img/ex_11.jpg')},
        //             {id:8, name: 'name8', text: 'test5', url: require('../../assets/img/ex_1.jpg')},
        //             {id:9, name: 'name9', text: 'test6', url: require('../../assets/img/ex_3.jpg')},
        //             {id:10, name: 'name10', text: 'test7', url: require('../../assets/img/ex_3.jpg')},
        //         ]
        //     }
        // },
    }
</script>
<style scoped>
    .item{
        width: 800px;
        height: 725x;
        margin: auto;
        text-align: center;
    }

    /* .item .item-group{
        /* width: 730px;
        height: 725px;
        margin: auto;
        margin-top: 5px;
        text-align: center;
        margin: auto;
    } */

    .item .item-card{
        width: 160px;
        height: 350px;
        max-width: 160px;
        max-height: 350px;
        margin: auto;
        margin-top: 5px;
        margin-left: 2px;
        margin-right: 2px;
        display: inline-block;
        text-align: center;
    }

    .item .item-card ul{
        list-style-type:none;
        margin: 0px;
        padding: 0px;
        text-align: center;
    }

    .item .item-card item-img{
        width: 130px;
        height: 130px;
        margin: auto;
        text-align: center;
    }

    .item :hover{
        cursor: grab;
    }
    .item :active{
        cursor:grabbing;
    }
</style>