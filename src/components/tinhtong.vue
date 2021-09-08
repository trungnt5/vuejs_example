<template>
 <div class="danrong">
    <h1>Nhập 2 số tự nhiên để tính tổng</h1>
	<b>Số thứ nhất: </b><br>
	<input type="text"  id="textIn1" v-on:blur=" IsNumeric('textIn1') "  /><br>
	<b>Số thứ hai: </b><br>
	<input type="text" id="textIn2"/><br><br>
    <input type="button" id="btnSum" value="Tính tổng" v-on:tinhtong=" laSo('textIn1','textIn2') " />
 </div>
</template>

<script>

export default{
    name:'tinhtong',
    methods: {
        tinhtong :function (textBox1, textBox2) {
            var x=document.getElementById(textBox1).value;
				var y=document.getElementById(textBox2).value;
				var sum=0;
				sum=Number(x)+Number(y);
				alert("Tổng 2 số là: " + sum);
        },
        laSo: function (inputtxt){
            var numbers = /^[0-9]+$/;
                if(!document.getElementById(inputtxt).value.match(numbers))
                {
                    alert('Ký tự không đúng yêu cầu, vui lòng chỉ nhập số tự nhiên');
                    document.getElementById(inputtxt).value = "";
                }
            
            
        } 
    }
    
    
        
};
</script>

<style>
   .danrong{ line-height: 1.5;}
</style>
