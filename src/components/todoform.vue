<template>
    <div class="danrong" id="list">
        <form @submit.prevent="themnvu">
            <label for="">Công việc: </label>
            <input type="text" v-model="nvumoi">  
            <button class="vienphai" type="submit" > Thêm</button>   
        </form>   
        <span>
            {{ nvumoi }}
        </span>
        <ul>
            <li  v-for="nvu1 in nvu1s" :key="nvu1.id">
                <input  type="checkbox" v-model="nvu1.done">
                <span class="vienphai">  {{ nvu1.id }}. </span>
                <span :class="{done:nvu1.done}">{{ nvu1.title }} </span>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'todolist',
        el:"#list",
        data(){
            return{
               nvumoi:'',
               idnvu:1,
               nvu1s:[]
            }
        },
        methods: {
           themnvu(){
               this.nvu1s.push({
                   id:(this.idnvu)++,
                   title: this.nvumoi,
                   done: false
               });
               this.nvumoi = ''
           } 
        }
    }
</script>

<style>
   .danrong{ line-height: 1.5;}
   .done {
       text-decoration: line-through;
   }
   .vienphai{
       margin-left:5px
   }
</style>
