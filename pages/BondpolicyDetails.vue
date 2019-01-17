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
                    <h1 class="WelcomeText">Smart Wealth - 22323223</h1>
    
    
                    <div class="CardArea">
    
    
                        <div v-for="CardData in CardPolicyInsurance" :key="CardData.id">
                            <div class="MyTALPolicyCard">
                                <h2>Policy Details</h2>
    
    
                                <div class="topDetails">
    
    
                                    <div class="policyDetails">
                                        <div v-for="(PolicyData, PolicyLabel) in CardData.policyData" :key="PolicyData.Policy">
                                            <div class="policyDataArea">
                                                <div class="policyLabelText">{{PolicyLabel}}:</div>
                                                <div>{{PolicyData}}</div>
                                            </div>
                                        </div>
                                    </div>
    
                                    <div class="contactDetails">
                                        <div v-for="(PolicyData, PolicyLabel) in CardData.contactDetails">
                                            <div class="contactDataArea">
                                                <div>
                                                    <div class="contactLabelText">{{PolicyLabel}}:</div>
                                                    <div>{{PolicyData}} </div>
                                                </div>
                                                <div><a class="editLink" href="#">Edit</a></div>
    
    
                                            </div>
                                        </div>
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
                            "Policy owner": "Mercer Superannuation (Australia) Limited",
                            "LUCAS JAMES FINLAY": "$1,545.00",
                            "Policy status": "In Force",
                            "Commencement date": "31/01/2017",
                            "Anniversary date": "31/01/2019"
                        },
                        contactDetails: {
                            "Postal address": "123 Easy Street, Melbourne, Vic, 3000",
                            "Email address": "email@email.com",
                            "Mobile Number": "0434 796 000",
                            "Home Number": "03 9789 3433",
                            "Work Number": ""
    
                        },
                        Alert: "",
                        AlertPrice: "",
                        Action: "If you would like to pay your premium now, please click on Pay Now.",
                        ActionButton: "btn-primary-outline"
    
                    }
                }
    
            }
        }
    }
</script>

<style>
    .WelcomeText {
        color: #232d32;
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
    
    .MyTALPolicyCard {
        background-color: white;
        color: #222;
        padding: 30px;
        margin-top: 30px;
        margin-right: 30px;
        flex: 1;
    }
    
    .topDetails {
        display: flex;
    }
    
    .policyDetails {
        margin-right: 30px;
        max-width: 350px;
    }
    
    .contactDetails {
        max-width: 350px;
    }
    
    .policyDataArea {
        display: flex;
        justify-content: space-between;
        border-bottom: 1px solid #e8e8e8;
        font-size: .875rem;
        padding-bottom: 5px;
        margin-top: 20px;
    }
    
    .contactDataArea {
        display: flex;
        justify-content: space-between;
        font-size: .875rem;
        padding:15px;
    }

    .contactDataArea:hover{
        background-color: rgb(247, 247, 247);
        padding:15px;
    }
    
    .policyLabelText {
        font-weight: 500;
        letter-spacing: normal;
        color: #222;
    }
    
    .contactLabelText {
        font-size: .75rem;
        line-height: 1.1666666667;
        font-weight: 400;
        display: block;
        margin-bottom: 5px;
        color: #6a7278;
    }
    
    .editLink {
        text-transform: uppercase;
        font-weight: 700;
        letter-spacing: 0.1em;
        font-size: 11px;
        font-size: .6875rem;
        line-height: 1.2727272727;
        border-bottom: 1px solid #80C342;
        vertical-align: bottom;
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
