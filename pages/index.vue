<template>
  <div class="Grid">
    <div class="topBar">
      <div class="phoneText">1300 209 088</div>
      <div class="UserEmail">XDDESIGN@GMAIL.COM</div>
      <a href="#">
        <div class="LogOutButton"> LOG OUT </div>
      </a>
    </div>
    <div class="navigation">
      <div><img src="~/assets/logo-primary.svg" alt="TAL"></div>
      <div class="myTALtext">myTAL</div>
      <a href="#">
        <div class="link helpBtn">Help</div>
      </a>
    </div>
    <div class="mainArea">
  
      <div class="LHSNav">LHS Nav</div>
      <div class="workArea">
        <div class="workAreaContent">
          <h1>Welcome LUCAS</h1>
          <div>View and update your TAL insurance policies</div>
  
          <div class="CardArea">
  
            <div v-for="CardData in Cards" :key="CardData.id">
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
  
          <div class="MyTALCard">
            <h2>Can't find all your policies?</h2>
            <p class="ActionText margin-top-30px">Click the add policy button to get started. If you don't have your policy number on hand please call 1300 209 088.</p>
            <div class="margin-top-30px"></div>
            <a href="#" class="btn-primary ">Add Policy</a>
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
  
  
  export default {
    components: {
      MyTalFooter
    },
    data: function() {
      return {
        Cards: {
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
  
          },
          Card2: {
            id: 2,
            Type: "Accelerated Protection",
            policyData: {
              "Policy Number": 332323223,
              "Premium": "$239.44 Monthly",
              "Status": "In Force",
              "Payment method": "Bank Account 349204153",
              "Due Date": "28/01/2019"
            },
            Alert: "Your premium is overdue",
            AlertPrice: "Amount: $718.32",
            Action: "If you would like to pay your premium now, please click on Pay Now.",
            ActionButton: "btn-primary-danger"
          },
        }
      }
    }
  }
</script>

<style>
.margin-top-30px{
  padding-top:30px
}

  h2 {
    font-size: 1.125rem;
    line-height: 1.3333333333;
  }

  .pay-now{
    color: #e50404;
    font-weight: bold;
  }
  
  .Grid {
    display: grid;
    grid-template-rows: 39px 85px auto 235px;
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
  
  .navigation {
    background-color: rgb(255, 255, 255);
    border-bottom: 1px solid rgb(232, 232, 232);
    padding-left: 60px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }
  
  .mainArea {
    display: grid;
    grid-template-columns: 330px 1fr;
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
  
  .CardArea {
    display: flex;
  }
  
  .MyTALCard {
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
</style>
