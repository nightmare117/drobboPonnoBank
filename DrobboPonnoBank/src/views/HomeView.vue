<script setup>
  import NavBar from '../components/navbar.vue'
  import Accounts from '../components/AccountModal.vue'
  import {ref} from 'vue'
  import Transaction from '../components/transaction.vue'
  const mainPageFlag = ref(true)
  // const user = ref("John Doe");
  const userProfile = ref(
    [
      {
        user: "John Doe",
        id: "12381237112",
        balance: 3002300
      },
      {
        user: "Abir Shah",
        id: "12381247112",
        balance: 30300
      },
      {
        user: "Maruf Khan",
        id: "12381237142",
        balance: 102300
      },
      {
        user: "Jubaer Ahmed",
        id: "12321237112",
        balance: 52300
      },
      {
        user: "Hayder Ali",
        id: "12381217112",
        balance: 3000300
      },
      {
        user: "Abdur Rahman",
        id: "12381221142",
        balance: 10200300
      }
    ]
  )

  const transactions = ref(
    [
      {
        id: 1,
        sid: 2,
        rid: 4,
        amount: 12313
      },
      {
        id: 2,
        sid: 2,
        rid: 4,
        amount: 353453
      },
      {
        id: 3,
        sid: 3,
        rid: 4,
        amount:  45224
      },
      {
        id: 4,
        sid: 2,
        rid: 4,
        amount: 234234
      },
      {
        id: 5,
        sid: 2,
        rid: 4,
        amount: 24234
      },
      {
        id: 6,
        sid: 2,
        rid: 4,
        amount: 243222
      }
    ]
  )

  const navSignal = (e)=>{
    mainPageFlag.value = !mainPageFlag.value
  }
</script>

<template>
  <div class="homeBank">
    <div class="homeBankWrapper">
      <NavBar :history="mainPageFlag" @response="(msg) => navSignal(msg)"/>
    <div class="bankUIMargin">

    </div>
      <div v-if="mainPageFlag" class="MainPage">
          <div class="TitleContainer">
          <h3 class="BankTitle">USER ACCOUNTS</h3>
          <div class="lineHome"></div>
        </div>
        
        <div class="AccountList">
          <li v-for="items in userProfile">
            <Accounts :userName="items.user"
              :bankId="items.id"
              :bankBalance="items.balance"/>
          </li>
        </div>
      </div>
      <div v-else class="historyPage">
        <h1>Transaction History</h1>
        <div class="transactionContainer">
          <li v-for="items in transactions">
            <Transaction :id="items.id"
              :sid="items.sid"
              :rid="items.rid"
              :amount="items.amount"/>
          </li>
        </div>
      </div>

    </div>
  </div>
</template>

<style>
li {
  list-style: none;
}
.transactionContainer{
  width: 80%;
  /* height: 100%; */
  display: flex;
  flex-direction: column;
}
.historyPage h1{
  margin-top: 40px;
}
.historyPage{
  height: calc(100vh - 60px);
  width: 100vw;
  /* background: rgba(221, 220, 220, 0.303); */
  display: flex;
  flex-direction: column;
  align-items: center;
}
.MainPage{
  display: flex;
  flex-direction: column;

}
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
    /* background: rgba(0, 0, 0, 0.199); */
    background-attachment: fixed;
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
    background-attachment: fixed;
    /* background-position: center; */
    overflow-x: hidden;
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
