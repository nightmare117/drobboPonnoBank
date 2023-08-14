<script setup>
    const props = defineProps({
    id:Number,
    sid: Number,
    rid: Number,
    amount: Number
//   shopNumber:String
});
</script>

<template>
    <div class="transaction-wrapper">
        <div class="transactionBody">
        <div class="transactionID">
            <h7>Transaction ID</h7>
            <p>{{ id }}</p>
        </div>
        <div class="transactionID">
            <h7>Sender Account</h7>
            <p>{{sid}}</p>
        </div>
        <div class="transactionID">
            <h7>Receiver Account</h7>
            <p>{{ rid }}</p>
        </div>
        <div style="border-right: none;" class="transactionID">
            <h7>Total Amount</h7>
            <p>{{ amount }} Tk</p>
        </div>
    </div>
    </div>
</template>

<style>
.transaction-wrapper{
    height: 100%;
    width:100%;
    display: flex;
    flex-direction: column;
}
p{
    margin: 0;
}
.transactionID p{
    margin-left: 10px;
    font-weight: 600;
}
.transactionID h7{
    font-size: 10px;
    margin: 5px;
    margin-left: 10px;
    font-weight: 600;
    color: rgba(170, 69, 11,1);
}
.transactionID{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    width: 25%;
    border-right: solid;
    border-width: 2px;
    box-shadow: rgba(0, 0, 0, 0.09) 0px 2px 1px, rgba(0, 0, 0, 0.09) 0px 4px 2px,
     rgba(0, 0, 0, 0.09) 0px 8px 4px, rgba(0, 0, 0, 0.09) 0px 16px 8px, rgba(0, 0, 0, 0.09) 0px 32px 16px;
    /* background: blue; */
}
.transactionBody{
    border-radius: 10px;
    height: 60px;
    width: 100%;
    min-width: 400px;
    background: white;
    margin-top: 20px;
    display: flex;
    z-index: 100px;
}
</style>