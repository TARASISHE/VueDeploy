<template>
        <div id="nav" class="nav"><!--v-if="$store.state.user"--> 
          <div class="container">
            <div class="flex-center-between">
              <ul class="list">
                <li class="list-link"><router-link to="/">Home</router-link> </li>
                <li class="list-link"><router-link to="/calculator">Calculator</router-link></li>
                <li class="list-link"><router-link to="/todo">Todo-List</router-link></li>
                <li class="list-link"><router-link to="/weather-forecast">Weather Forecast</router-link></li>
              </ul>
                <button class="btn-logout" @click="$store.dispatch('logout')" >Logout</button><!--@click="$store.dispatch('logout')"--> 
            </div>
          </div>
       </div>   
       
  </template>
  <!--
  <script>
  import { onBeforeMount } from 'vue'
  import { useStore } from 'vuex'
  export default {
    setup() {
      const store = useStore()
      onBeforeMount(() => {
        store.dispatch('fetchUser')
      })
    }
  }
  <script/>
  -->

  <style>

  .container{
    max-width: 1280px;
    margin: 0 auto;
  }
  .nav{
    width: 100%;
    height: 50px;
    background-color: var(--medium-dark); 
    padding-bottom: 50px;
    padding: 0px 15px;
  }
 
  .list{
    display: flex;
    gap: 40px;
  }
 
  .list-link a{
    font-size: 16px;
    color: var(--light-color);
  }
  
  .list-link a:hover{
    color: #FFF;
    text-decoration: underline;
  }
  .btn-logout{
    border: none;
    font-size: 16px;
    color: var(--medium-dark) ;
    width: 100px;
    height: 25px;
    border-radius: 5px;
    background-color: var(--medium-light);
    color: #FFF;
    background-image: linear-gradient(#c4dfe6,#c4dfe6);
    background-size: 0 100%;
    background-repeat: no-repeat;
    transition: .4s;
    cursor: pointer;
  }
  .btn-logout:hover{
    background-size: 100% 100%;
    color: var(--medium-dark);
  }
  
  @media  screen and (max-width: 1281px){
    .flex-center-between{
      padding: 0px 15px;
    }
  }

  @media  screen and (max-width: 768px ){
    .list{
    gap: 20px;
    }
    .list-link a{
    font-size: 14px;
    }
  }

  @media  screen and (max-width: 500px){
   .flex-center-between{
    flex-direction: column;
   }
   .nav{
    height: 75px; 
  }
  .list{
   align-items: center;
   margin: 10px 0px;
  }
  }

  @media  screen and (max-width: 375px){

    .list-link a{
    font-size: 12px;
    }
    .btn-logout{
    font-size: 12px;
    width: 75px;
    height: 55px;
  }
  }
  
  
  </style>