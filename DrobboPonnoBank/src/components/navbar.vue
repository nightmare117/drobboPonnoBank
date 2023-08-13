<script setup>

</script>

<template>
    <div class="navBack">
        <div  class="navTitle">
            <p >Drobbo<span class="navTitleSpan">Ponno</span></p>
        </div>
        <div class="navCenter">
            <!-- some free space for future works -->
        </div>
        <div class="navButtons">
            
            <div class="navButtonPaddin">
                <img  class="notificationButton" src="../assets/notification.png" title="notifications" alt="notification"/>
            </div>
            
      

            <!-- <p>John Doe</p> -->
        </div>
    </div>
</template>

<style>
body{
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.navButtonPaddin{
    width: 40px;
    height: 22px;
}
.notificationButton:hover{
    height: 21px;
}
.cartButton:hover{
    height: 21px;
}
.bankButton:hover{
    /* padding-bottom: 5px; */
    /* background: rgba(170, 69, 11,.6); */
    /* border-radius: 100px; */
    height: 20px;
}
.bankButton{
    height: 19px;
    cursor: pointer;
}
.navButtons p{
    color: white;
    margin-right: 40px;
    margin-left: 80px;
}
.cartButton{
    height: 20px;
    /* margin-left: 15px; */
    cursor: pointer;
}
.notificationButton{
    height: 20px;
    cursor: pointer;
    margin-left: -20px;
}
.navButtons{
    display: flex;
    width: 80%;
    justify-content: flex-end;
}
.navCenter{
    /* width: 40%; */
}
.navTitleSpan{
    color: rgba(170, 69, 11,1);
    font-weight: 500;
}
.navTitle p{
    color: white;
    margin-left: 20px;
    font-size: 17px;
    font-weight: 300;
    /* letter-spacing: 2px; */
}
.navTitle{
    width: 20%;
    cursor: pointer;
}
.navBack{
    position: fixed;
    width: 100vw;
    height: 60px;
    background: rgba(0, 0, 0, 0.84);
    display: flex;
    align-items: center;
    z-index: 1;
}
.dropdown {
  margin-right: 40px;
  margin-left: 80px;
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}

.dropdown:hover .dropdown-content {
  display: block;
}

/* Additional button styling */
.dropdown-button {
  background-color: transparent;
  color: white;
  /* padding: 12px; */
  font-size: 14px;
  border: none;
  cursor: pointer;
}

.dropdown-button:hover {
  /* background-color: #45a049; */
}

.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {
  background-color: #f1f1f1;
}
</style>
