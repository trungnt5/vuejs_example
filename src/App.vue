<template>
    <div class="container">
        <div   div id="vidu">
            <button v-on:click="chao">{{ nut1 }}</button>
        </div> 

        <div id="vidu2">
            <select v-on:change="menu1">
            <option>--- Chọn thành phố ---</option>
            <option value="1">Hà Nội</option>
            <option value="2">Hải Phòng</option>
            <option value="3">Đà Nẵng</option>
            </select>  
        </div>
        <tinhtong />
       <todolist />
       <todoform />
    </div>
</template>

<script>
 import tinhtong from './components/tinhtong.vue'
 import todolist from './components/todolist.vue'
 import todoform from './components/todoform.vue'

export default{
    name:"App",
   components: {  tinhtong,todolist,todoform },
    data(){
        return{
            nut1:"Bấm"
        }
    },
    methods: {
        chao: function () {
            alert('Xin chào')
        },
        menu1: function (event) {
            console.log(event.target.value);
        }
    }
        
}
</script>

<style>
 .container{
        margin-left: 80px;
    }
</style>
