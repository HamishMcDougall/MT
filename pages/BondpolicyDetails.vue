<template>
  <div class="Grid">
    <div class="topBar">
      <div class="phoneText">1300 209 088</div>
      <div class="UserEmail">XDDESIGN@GMAIL.COM</div>
      <a href="#">
        <div class="LogOutButton"> LOG OUT </div>
      </a>
    </div>
    <div class="navigationDesktop">
      <div><img src="~/assets/logo-primary.svg" alt="TAL"></div>
      <div class="myTALtext">myTAL</div>
      <a href="#">
        <div class="link helpBtn">Help</div>
      </a>
    </div>
  
  
    <div class="navigationMobile">
      <div class="btn-primary-outline">Menu</div>
  
      <div><img src="~/assets/logo-primary.svg" alt="TAL"></div>
  
      <a href="#">
        <div class="link helpBtn">Help</div>
      </a>
    </div>
  
  
    <div class="mainArea">
  
      <div class="LHSNav">
  
  
        <myTALNav></myTALNav>
  
      </div>
  
      <div class="workArea">
        <div class="workAreaContent">
          <h1 class="WelcomeText">Accelerated Protection - 22323223</h1>
 
  
          <div class="CardArea">




  
            <div v-for="CardData in CardsInsurance" :key="CardData.id">
              <div class="MyTALCard">
                <h2>{{CardData.Type}}</h2>
                <div v-for="(PolicyData, PolicyLabel) in CardData.policyData" :key="PolicyData.Policy">
                  <div class="policyDataArea">
                    <div class="policyLabelText">{{PolicyLabel}}:</div>
                    <div>{{PolicyData}}</div>
                  </div>
                </div>
                <div class="StatusText">
                  <div class="AlertTextArea">
                    <div class="ActionText pay-now">{{CardData.Alert}}</div>
                    <div class="ActionText"><strong>{{CardData.AlertPrice}}</strong></div>
                  </div>
                  <div class="ActionTextArea">
                    <div class="ActionText">{{CardData.Action}}</div>
                    <a href="#" :class="[CardData.ActionButton]">Pay Now</a>
                  </div>
                </div>
                <div style="padding-top:40px">
                  <a href="#" class="btn-primary">View Details</a>
                </div>
              </div>
            </div>
          </div>
  
  
 
  
  

  
        </div>
  
      </div>
  
    </div>
    <div class="footer">
      <MyTalFooter></MyTalFooter>
    </div>
  </div>
</template>

<script>
  import MyTalFooter from '~/components/MyTalFooter.vue'
  import myTALNav from '~/components/myTAL-Nav.vue'
  
  
  
  export default {
    components: {
      MyTalFooter,
      myTALNav
    },
    data: function() {
      return {
  
        CardPolicyInsurance: {
          Card1: {
            id: 1,
            Type: "Accelerated Protection",
            policyData: {
              "Policy Number": 22323223,
              "Sum insured": "$1,545.00",
              "Premium": "$1,556.83 Annual",
              "Status": "In Force",
              "Payment method": "Direct",
              "Due Date": "28/01/2019"
            },
            Alert: "",
            AlertPrice: "",
            Action: "If you would like to pay your premium now, please click on Pay Now.",
            ActionButton: "btn-primary-outline"
  
          }
      }
    },
    methods: {
  
    }
  
  }
</script>

<style>

.WelcomeText{
  color:#232d32;
}
  .TreeNavigation li {
    padding-left: 20px !important;
    color: white !important;
  }
  
  .margin-top-30px {
    padding-top: 30px
  }
  
  h2 {
    font-size: 1.125rem;
    line-height: 1.3333333333;
  }
  
  .pay-now {
    color: #e50404;
    font-weight: bold;
  }
  
  .Grid {
    display: grid;
    grid-template-rows: 39px 85px 0px auto 235px;
    min-height: 100vh;
  }
  
  .topBar {
    background-color: rgb(34, 34, 34);
    color: rgb(255, 255, 255);
    padding-left: 60px;
    display: flex;
    justify-content: flex-start;
    align-items: baseline;
    font-size: .625rem;
  }
  
  .navigationDesktop {
    background-color: rgb(255, 255, 255);
    border-bottom: 1px solid rgb(232, 232, 232);
    padding-left: 60px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }
  
  .navigationMobile {
    visibility: hidden;
  }
  
  .mainArea {
    display: grid;
    grid-template-columns: 330px 1fr;
  }
  
  .workArea {
   /* background-image: url(/bg-cliff.jpg);*/
   background-color: rgb(235, 235, 235);
    background-repeat: no-repeat;
    background-size: cover;
    color: white;
  }
  
  .workAreaContent {
    max-width: 1100px;
    padding: 60px;
  }
  
  .CardArea {
    display: flex;
    align-content: stretch;
  }
  
  .MyTALCard {
    background-color: white;
    color: #222;
    padding: 30px;
    margin-top: 30px;
    margin-right: 30px;
    max-width: 456px;
    min-width: 256px;
    flex: 1;

  }
  
  hr {
    width: 940px;
    margin-top: 30px;

  }
  
  .MyTALCard-Base {
    background-color: white;
    color: #222;
    padding: 30px;
    margin-top: 30px;
    margin-right: 30px;
  }
  
  .policyDataArea {
    display: flex;
    justify-content: space-between;
    border-bottom: 1px solid #e8e8e8;
    font-size: .875rem;
    padding-bottom: 5px;
    margin-top: 20px;
  }
  
  .policyLabelText {
    font-weight: 500;
    letter-spacing: normal;
    color: #222;
  }
  
  .StatusText {
    padding-top: 20px;
  }
  
  .AlertTextArea {
    display: flex;
    flex-direction: column;
  }
  
  .ActionTextArea {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
  
  .ActionText {
    font-size: 14px;
    line-height: 1.4285714286;
    padding-right: 20px;
  }
  
  .btn-primary {
    padding: 12px 20px 8px;
    border-radius: 3px;
    border: 1px solid #80C342;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: #232d32;
    background-color: #80C342;
    font-weight: 700;
    -webkit-font-smoothing: subpixel-antialiased;
    font-size: .75rem;
    display: inline-block;
  }
  
  .btn-primary:hover {
    background: #c1e2a3;
    border-color: #c1e2a3;
    color: #232d32;
  }
  
  .btn-primary-outline {
    background-color: transparent;
    border-color: #80C342;
    color: #232d32;
    padding: 12px;
    border-radius: 3px;
    border: 1px solid #80C342;
    text-transform: uppercase;
    font-weight: 700;
    font-size: .75rem;
    flex-shrink: 0;
    display: inline-block;
  }
  
  .btn-primary-outline:hover {
    border-color: #c1e2a3;
    color: #232d32;
  }
  
  .btn-primary-danger {
    background-color: #e50404;
    border-color: #e50404;
    color: #fff;
    padding: 12px;
    display: inline-block;
    border-radius: 3px;
    text-transform: uppercase;
    font-weight: 700;
    font-size: .75rem;
    flex-shrink: 0;
  }
  
  a {
    text-decoration: none;
    color: #232d32;
  }
  
  a:hover {
    text-decoration: none;
  }
  
  .phoneText {
    flex-grow: 1;
  }
  
  .UserEmail {
    padding-right: 50px;
  }
  
  .LogOutButton {
    margin-right: 50px;
    border-width: 1px;
    border-style: solid;
    border-color: rgb(123, 123, 123);
    border-image: initial;
    padding: 0px 10px;
    background: transparent;
    color: white;
    text-transform: uppercase;
    line-height: 24px;
    margin-top: 7px;
    font-weight: 700;
  }
  
  .LogOutButton:hover {
    border-color: #80C342;
    color: #80C342;
  }
  
  .myTALtext {
    flex-grow: 1;
  }
  
  .helpBtn {
    margin-right: 50px;
  }
  
  .link {
    font-size: .875rem;
    font-weight: 500;
    color: #222;
    text-decoration: none;
    border-bottom: 2px solid #80C342;
    text-transform: uppercase;
  }
  
  .link:hover {
    border-bottom: 2px solid #80C342;
    background-color: #80C342;
  }
  
  .LHSNav {
    padding-left: 60px;
    padding-top: 30px;
    background-color: #232d32;
    color: white;
    font-size: .9375rem;
    line-height: 1.33;
  }
  
  /*
  @media only screen and (max-width: 1200px) {
    .Grid {
      display: grid;
      grid-template-rows: 0px 0px 62px auto 235px;
      min-height: 100vh;
    }
    .topBar {
      visibility: hidden;
    }
    .navigationDesktop {
      visibility: hidden;
    }
    .navigationMobile {
      visibility: visible;
      background-color: rgb(255, 255, 255);
      border-bottom: 1px solid rgb(232, 232, 232);
      padding-left: 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .myTALtext {
      flex-grow: 0;
    }
    .mainArea {
      display: grid;
      grid-template-columns: 0px 1fr;
    }
    .workArea {
      background-image: url(/bg-cliff.jpg);
      background-repeat: no-repeat;
      background-size: cover;
      color: white;
    }
    .workAreaContent {
      max-width: 1100px;
      padding: 60px;
    }
   
  } */
</style>
