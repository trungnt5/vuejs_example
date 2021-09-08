<template>
    <div class="container">
        <div   div id="vidu">
            <button v-on:click="chao">Button1</button>
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
    </div>
</template>

<script>
import tinhtong from './components/tinhtong.vue'

export default{
    name:"App",
    components: { tinhtong },
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
