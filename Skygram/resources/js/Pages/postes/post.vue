<template>
    <app-layout> 
         <template #header>
            <h2  class="font-semibold text-xl text-gray-800 leading-tight"> Post </h2>
         </template>
         
        <div class="py-12">
            <div class="max-w-5xl mx-auto sm:px-6 lg:px-8 space-y-6">
              
         <div >
        
         <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg ">
          <div class="mx-14 text-2xl font-bold "> {{ post.user.name }}</div>
         <h2 class="mx-14 py-1"> {{ post.caption }} </h2>
        
         <div><img  v-bind:src=" post.attachment "  class="w-52 py-6 mx-14"> </div>
       
        <div class="py-1 mx-14"> <a href="#" class="bg-indigo-500 p-2 text-sm text-white my-3">Like </a> 
        
          <div class="py-2  text-2xl font-bold">Comments </div>
          {{ post.comments[0].content}}
        </div> 
        </div> 
        </div> <br>
            </div></div>
    </app-layout>
 </template>
 <script>
 
 import AppLayout from './../../Layouts/AppLayout'; 
 export default {
       components : {
           AppLayout 
       }, 

       props : ['post'], 

       data() {
           return {
               
           }
       }, 

     
     
 }
 </script>