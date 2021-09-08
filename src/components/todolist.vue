<template>
    <div class="danrong" id="list">
        <ul>      
            <li v-for="nvu in nvus"  :key="nvu.id" >{{ nvu.id }} - {{ nvu.tên }} - {{ nvu.completed }}</li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'todolist',
        el:"#list",
        data(){
            return{
                nvus:[
                    {id:"1", tên:"Ngủ",completed:"Hoàn thành"},
                    {id:"2", tên:"Ăn uống",completed:"Chưa hoàn thành"},
                    {id:"3", tên:"Làm việc",completed:"Hoàn thành"},
                    {id:"3", tên:"Học tập",completed:"Hoàn thành"},
                ],
            }
        },
    }
</script>

<style>
   .danrong{ line-height: 1.5;}
</style>
