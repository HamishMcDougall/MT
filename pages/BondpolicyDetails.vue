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
            <div><a href="dashboard"> <img src="~/assets/logo-primary.svg" alt="TAL"></a></div>
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
    
    
    
                                <div class="topDetails">
    
    
                                    <div class="">
                                        <div v-for="(PolicyData, PolicyLabel) in CardData.policyData" :key="PolicyData.Policy">
                                            <div class="Balance">
                                                <div class="">
                                                    <h1>{{PolicyLabel}}:</h1>
                                                </div>
                                                <div>
                                                    <h1>{{PolicyData}}</h1>
                                                </div>
                                            </div>
                                        </div>
    
                                    </div>
                                    <ballanceHistory></ballanceHistory>
    
    
    
    
                                </div>
    
                                <div class="middleDetails">
    
                                    <div class="leftDetails">
                                        <h2>Recent activity</h2>
    
                                        <div class="ActivityFeedArea" v-for="ActivityData) in Activity">
                                            <div class="DateText">{{ActivityData.Date}} </div>
                                            <div class="FeeText"> {{ActivityData.FType}}
                                                <div style="float:right" :class="[ActivityData.AType]">{{ActivityData.Amount}}</div>
                                            </div>
                                            <div class="AtypeText"> {{ActivityData.Type}}</div>
                                            
                                        </div>
    
                                    </div>
    
    
                                    <div class="rightDetails">
                                        <h2>How my account is invested</h2>
                                        <accountInvestmentChart></accountInvestmentChart>
                                    </div>
    
                                </div>
    
    
                                <div class="middleDetails">
                                    <div class="leftDetails">
                                        <h2>Asset allocation</h2>
                                        <assetAllocationChart></assetAllocationChart>
                                    </div>
    
                                    <div class="rightDetails">
                                        <h2>Personal Details</h2>
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
    import accountInvestmentChart from '~/components/accountInvestmentChart.vue'
    import ballanceHistory from '~/components/ballanceHistory.vue'
    import assetAllocationChart from '~/components/assetAllocationChart.vue'
    
    
    export default {
        components: {
            MyTalFooter,
            myTALNav,
            accountInvestmentChart,
            ballanceHistory,
            assetAllocationChart
        },
        data: function() {
            return {
    
                CardPolicyInsurance: {
                    Card1: {
                        id: 1,
                        Type: "Accelerated Protection",
                        policyData: {
                            "Current Balance": "$32,454.45",
    
                        },
                        contactDetails: {
                            "Postal address": "123 Easy Street, Melbourne, Vic, 3000",
                            "Email address": "email@email.com",
                            "Mobile Number": "0434 796 000",
                            "Home Number": "03 9789 3433",
                            "Work Number": ""
    
                        },
                    }
                },
                Activity: {
                    Data1: {
                        Date: "31 March 2018",
                        FType: "Ongoing Member Advice Fee",
                        Amount: "-$27.83",
                        AType: "Negative",
                        Type: "Southerly"
                    },
                    Data2: {
                        Date: "2 April 2018",
                        FType: "Regular Investment",
                        Amount: "$6,000.00",
                        AType: "Positive",
                        Type: "Direct Debit"
                    },
                    Data3: {
                        Date: "31 March 2017",
                        FType: "Ongoing Member Advice Fee",
                        Amount: "-$27.83",
                        AType: "Negative",
                        Type: "Southerly"
                    },
                    Data4: {
                        Date: "2 April 2017",
                        FType: "Regular Investment",
                        Amount: "$6,000.00",
                        AType: "Positive",
                        Type: "Direct Debit"
                    },
                    Data5: {
                        Date: "31 March 2017",
                        FType: "Ongoing Member Advice Fee",
                        Amount: "-$27.83",
                        AType: "Negative",
                        Type: "Southerly"
                    },
                    Data6: {
                        Date: "2 April 2017",
                        FType: "Regular Investment",
                        Amount: "$6,000.00",
                        AType: "Positive",
                        Type: "Direct Debit"
                    },
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
        min-width: 700px;
    }
    
    .middleDetails {
        display: flex;
        padding-bottom: 20px;
        padding-top:20px;
    }
    
    .leftDetails {
        margin-right: 30px;
        min-width: 300px;
        
    }
    
    .rightDetails {
        min-width: 300px;
    }
    
    .policyDataArea {
        display: flex;
        justify-content: space-between;
        border-bottom: 1px solid #e8e8e8;
        font-size: .875rem;
        padding-bottom: 5px;
        margin-top: 20px;
    }
    
    .Balance {
        display: flex;
        justify-content: space-between;
        font-size: .875rem;
        margin-bottom: 20px;
    }
    
    .contactDataArea {
        display: flex;
        justify-content: space-between;
        font-size: .875rem;
        padding: 15px;
    }
    
    .contactDataArea:hover {
        background-color: rgb(247, 247, 247);
        padding: 15px;
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
    
    .ActivityFeedArea {
        font-size: .875rem;
         border-bottom: 1px solid #e8e8e8;
    }
    
    .Negative {
        color: red;
    }
    
    .DateText {
        text-transform: uppercase;
        font-weight: 700;
        letter-spacing: 0.1em;
        font-size: 8px;
        margin-top: 10px;
        opacity: 0.7;
    }
    
    .AtypeText {
        opacity: 0.5;
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
