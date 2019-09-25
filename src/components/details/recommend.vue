<template>
    <div class="recommend">
        <div class="recommend-item" v-for="item in items" :key="id">
            <img src="../../assets/img/例11.jpg" alt="">
        </div>
    </div>
</template>

<script scoped>
    import draggable from 'vuedraggable'

export default{
    name: "dnd",
    components: {
        draggable,
    },
    data(){
        return{  
            items: [
                {id:1, name: 'name1', text: 'てすとてす', url:'../../assets/img/例1.jpg'},
                {id:2, name: 'イラン帝国', text: 'test2', url:'../../assets/img/例３.jpg'},
                {id:3, name: 'name3', text: 'test3', url:'../../assets/img/例11.jpg'},
                {id:4, name: 'name4', text: 'test4', url:'../../assets/img/例13.jpg'},
                {id:5, name: 'name5', text: 'test5', url:'../../assets/img/例1.jpg'},
            ]
        }
    }
}   
</script>

<style lang="css" scoped>
    .recommend{
        margin: auto;
        display: flex;
    }

    .recommend .recommend-item{
        width: 60px;
        height: 60px;
        margin: auto;
        margin-left: 2px;
    }

    .recommend .recommend-item img{
        width: 100%;
        height: 100%;
    }

    .item :hover{
        cursor: grab;
    }

    .item :active{
        cursor:grabbing;
    }
</style>