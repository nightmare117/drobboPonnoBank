<template>
    <div class="user-profile">
      <!-- <h2>User Profile</h2> -->
      <p class="AccountUserName"><strong>Name : </strong><span style="color: rgba(170, 69, 11,1);">{{ userName }}</span> </p>
      <p class="AccountUserName"><strong>Bank ID : </strong> {{ bankId }}</p>
      <p class="AccountUserName"><strong>Bank Balance : </strong> ${{ bankBalance }}</p>
    </div>
  </template>
  
  <script>
  import { defineComponent, ref } from 'vue';
  
  export default defineComponent({
    props: {
      userName: String,
      bankId: String,
      bankBalance: Number,
    },
    setup(props) {
      // Create reactive variables
      const userName = ref(props.userName);
      const bankId = ref(props.bankId);
      const bankBalance = ref(props.bankBalance);
  
      return {
        userName,
        bankId,
        bankBalance,
      };
    },
  });
  </script>
  
  <style>
  .AccountUserName{
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  .user-profile {
    border: 1px solid #ccc;
    background: white;
    width: 400px;
    margin: 20px;
    padding: 20px;
    box-shadow: rgba(0, 0, 0, 0.02) 0px 1px 3px 0px, rgba(27, 31, 35, 0.15) 0px 0px 0px 1px;
  }
  
  </style>

