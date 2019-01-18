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
      <div><a href="dashboard"><img src="~/assets/logo-primary.svg" alt="TAL"><a></div>
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
          <h1 class="WelcomeText">Welcome LUCAS</h1>
 
  
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
  
  
 
  
  
          <div class="CardArea">
  
            <div v-for="CardData in CardsWealth" :key="CardData.id">
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
                  <a href="bondPolicyDetails" class="btn-primary">View Details</a>
                </div>
              </div>
            </div>
  
  
  
          </div>

          <div class="MyTALCard-Base">
            <h2>Can't find all your TAL products</h2>
            <p class="ActionText margin-top-30px">Click the add button to get started.
  
              <br> If you don't have your policy or investment number on hand please call 1300 209 088.</p>
            <div class="margin-top-30px"></div>
            <a href="#" class="btn-primary ">Add </a>
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
  
        CardsInsurance: {
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
          }
        },
  
        CardsWealth: {
          Card1: {
            id: 3,
            Type: "Smart Wealth",
            policyData: {
              "Nick Name": "Sarah School fund",
              "Account Number": 332323223,
              "Ballance": "$239.44",
              "Start Date": "10/1/2019",
              "10 Year Tax Date ": "10/1/2029",
              "Purpose": "Education Savings",
              "Goal Amount": "$120,000",
              "Adviser Name": "Mr. Jack Black"
            },
            Alert: "",
            AlertPrice: "",
            Action: "Your next payment will be on the 12/09/2019",
            ActionButton: "btn-primary-outline"
          },
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
  
  
  
  .phoneText {
    flex-grow: 1;
  }
  
  .UserEmail {
    padding-right: 50px;
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
