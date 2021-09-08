<template>
 <div class="danrong">
    <h1>Nhập 2 số tự nhiên để tính tổng</h1>
	<b>Số thứ nhất: </b><br>
	<!-- <input type="text" :value="so1.value" id="textIn1" v-on":blur=" laSo('#textIn1') "   /><br> -->
    <input id="textIn1"  v-model.number="so1"  @blur="laSo(so1)"/><br>
	<b>Số thứ hai: </b><br>
    <input id="textIn2"  v-model.number="so2"  @blur="laSo(so2)"  /><br>
	<!-- <input type="text" :value="so2.value" id="textIn2" v-on:blur=" laSo('#textIn2') " /><br> -->
    <input type="button" id="btnSum" value="Tính tổng" v-on:click=" tinhtong1 "/> <br>
    <span>Tổng 2 số: </span>
    <input v-model.number="tong" readonly/><br>
    
 </div>
</template>

<script>

export default{
    name:'tinhtong',
    data(){
        return {
            so1:1,
            so2:2,
            tong:null

        }
    },
    computed:{
       

    },
    methods: {
        tinhtong1 :function () {
            console.log("so1: ",this.so1)
            this.tong =  this.so1 + this.so2
        },
        laSo: function (event){
            var numbers = /^[0-9]+$/;
            if(!event.match(numbers))
            {
                alert('Ký tự không đúng yêu cầu, vui lòng chỉ nhập số tự nhiên');
                event= "";
            }
            
            
        },
        // thaydoi1:function(event){
        //     this.so1.value = event.target.value
        // },
        // thaydoi2:function(event){
        //     this.so2.value = event.target.value
        // },
        
        
    }
    
    
        
};
</script>

<style>
   .danrong{ line-height: 1.5;}
</style>
