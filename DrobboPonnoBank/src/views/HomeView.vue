<script setup>
  import NavBar from '../components/navbar.vue'
  import Accounts from '../components/AccountModal.vue'
  import {ref} from 'vue'

  const user = ref("John Doe");
</script>

<template>
  <div class="homeBank">
    <div class="homeBankWrapper">
      <NavBar/>
    <div class="bankUIMargin">

    </div>
    <div class="TitleContainer">
      <h3 class="BankTitle">USER ACCOUNTS</h3>
      <div class="lineHome"></div>
    </div>
    
    <div class="AccountList">
      <Accounts :userName="user"
      :bankId="34523752355"
      :bankBalance="2000000"/>

      <Accounts :userName="user"
      :bankId="34523752355"
      :bankBalance="2000000"/>

      <Accounts :userName="user"
      :bankId="34523752355"
      :bankBalance="2000000"/>

      <Accounts :userName="user"
      :bankId="34523752355"
      :bankBalance="2000000"/>
    </div>

    </div>
  </div>
</template>

<style>
.TitleContainer{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  background: rgba(0, 0, 0, 0.26);
}
.lineHome{
  height: 5px;
  width: 160px;
  background: rgba(170, 69, 11,1);
  margin-top: 20px;
  margin-bottom: 20px;
  border-radius: 10px;
}
.homeBankWrapper{
  height: 100%;
  width: 100%;
  display: flex;
    flex-direction: column;
    align-items: center;
    background: rgba(0, 0, 0, 0.199);
}
  .BankTitle{
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-size: 30px;
    color: white;
    z-index: 100;
    margin-bottom: 0px;
  }
  .AccountList{
    /* background: red; */
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
  }
  .bankUIMargin{
    height: 60px;
    width: 100vw;
    /* background: red; */
  }

  .homeBank{
    height: 100vh;
    width: 100vw;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-size: cover;
    animation: change 90s linear infinite alternate-reverse;
  }
  
  @keyframes change{
  0%{
    background: url(../assets/bank.jpg);
    background-repeat: no-repeat;
    background-size: 110% 110%;
  }
  /* 50%{
    background: url(../assets/image2.jpg);
    background-repeat: no-repeat;
    background-size: cover;
  } */
  40%{
    background: url(../assets/bank.jpg);
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }80%{
    background: url(../assets/bank.jpg);
    background-repeat: no-repeat;
    background-size: 110% 110%;
  }100%{
    background: url(../assets/bank.jpg);
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }
  }
</style>
