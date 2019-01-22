<template>
  <div class="mainArea">
    <!-- NAVIGATION  -->
    <div class="LHSNav">
      <myTALNav></myTALNav>
    </div>
    <!--END NAVIGATION-->
    <div class="workArea">
      <div class="workAreaContent">
        <div class="MyTALCard square" v-for="CardData in CardsInsurance" :key="CardData.id">
          <div class="CardDataTextAll">
            <svg width="20px" height="20px" viewBox="0 0 14 14" style="float:right" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                      <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                          <g id="Life-white-3" fill="#303E46" fill-rule="nonzero" >
                              <path d="M6.63,13.26 C2.96835211,13.26 -1.27675648e-15,10.2916479 -1.77635684e-15,6.63 C-2.22044605e-15,2.96835211 2.96835211,-1.11022302e-15 6.63,-1.77635684e-15 C10.2916479,-2.3869795e-15 13.26,2.96835211 13.26,6.63 C13.254493,10.2893644 10.2893644,13.254493 6.63,13.26 Z M6.63,1.03 C3.5372054,1.03 1.03,3.5372054 1.03,6.63 C1.03,9.7227946 3.5372054,12.23 6.63,12.23 C9.7227946,12.23 12.23,9.7227946 12.23,6.63 C12.23,5.14478766 11.6400017,3.72040574 10.589798,2.67020203 C9.53959426,1.61999831 8.11521234,1.03 6.63,1.03 Z M6.5,10.37 C6.33960435,10.3671733 6.18474664,10.3108614 6.06,10.21 L5.8,10.01 L5,9.38 C3.26,7.91 2.57,6.47 3,5.11 C3.12037884,4.65838687 3.37491875,4.25391248 3.73,3.95 C4.09920045,3.65470565 4.55724127,3.49262966 5.03,3.49 C5.58779493,3.50294945 6.12147989,3.71998133 6.53,4.1 C6.93628007,3.72899899 7.46029523,3.51301977 8.01,3.49 C8.49097308,3.49011332 8.95718834,3.65611421 9.33,3.96 C9.69763429,4.25837385 9.9632583,4.66379997 10.09,5.12 C10.48,6.48 9.79,7.91 8.04,9.38 C7.82,9.57 7.6,9.74 7.25,10.01 L6.98,10.21 C6.85604512,10.3122546 6.70068369,10.3687497 6.54,10.37 L6.5,10.37 Z M5.04,4.45 C4.78458237,4.44874355 4.5368349,4.53722479 4.34,4.7 C4.12095478,4.87254031 3.96319118,5.11093863 3.89,5.38 C3.63,6.34 4.2,7.44 5.63,8.64 L6.4,9.25 L6.53,9.35 L6.63,9.25 C6.97,8.99 7.18,8.82 7.39,8.64 C8.82,7.44 9.39,6.34 9.14,5.38 C9.06024571,5.1139606 8.90369826,4.87740001 8.69,4.7 C8.49059789,4.54300091 8.24378592,4.45837966 7.99,4.46 C7.54384354,4.4909422 7.1373884,4.72742519 6.89,5.1 C6.80094433,5.22691111 6.65503006,5.30173894 6.5,5.3 C6.34455335,5.30353071 6.19784372,5.228295 6.11,5.1 C5.86418656,4.73871648 5.47391668,4.50163665 5.04,4.45 Z" id="Shape"></path>
                          </g>
                      </g>
                  </svg>
            <h2>{{CardData.Type}}</h2>
            <div v-for="(PolicyData, PolicyLabel) in CardData.policyData" :key="PolicyData.Policy" class="CardPolicyTextAll">
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
        <div class="MyTALCard square" v-for="CardData in CardsWealth" :key="CardData.id">
          <div class="CardDataTextAll">
            <svg width="20px" height="20px" viewBox="0 0 14 14" style="float: right" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                      <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                          <g id="SWealth-white-03" fill="#303E46" >
                              <path d="M6.94,11.18 C6.37895072,11.1571517 5.84113028,10.9497569 5.41,10.59 L4.73,11.59 C5.27061157,12.0187329 5.92332019,12.2825938 6.61,12.35 L6.61,13.35 L7.61,13.35 L7.61,12.34 C8.60556403,12.2154384 9.33503925,11.3418154 9.28,10.34 C9.28,8.34 6.47,8.45 6.47,7.47 C6.47,7.01 6.75,6.82 7.26,6.82 C7.70162469,6.82688162 8.12102917,7.01489053 8.42,7.34 L9.21,6.47 C8.79309386,6.00748776 8.22663315,5.70655551 7.61,5.62 L7.61,4.59 L6.61,4.59 L6.61,5.59 C5.62145939,5.71511786 4.90711359,6.59702625 4.99,7.59 C4.99,9.41 7.8,9.39 7.8,10.45 C7.8,10.95 7.54,11.18 6.94,11.18 Z" id="Path"></path>
                              <path d="M9.8,8.98 C9.57273799,9.00977659 9.34879671,8.90523859 9.22568514,8.71190415 C9.10257356,8.51856971 9.10257356,8.27143029 9.22568514,8.07809585 C9.34879671,7.88476141 9.57273799,7.78022341 9.8,7.81 L10.96,7.81 C11.1063258,7.81201699 11.2518692,7.78832388 11.39,7.74 C11.7821609,7.6348066 12.1122514,7.37000869 12.3,7.01 C12.5619715,6.53592329 12.553765,5.95866866 12.2784227,5.49223064 C12.0030805,5.02579261 11.5016435,4.73969604 10.96,4.74 C10.8108761,4.74369572 10.6629085,4.76723601 10.52,4.81 L10.42,4.81 C10.2922955,4.86174171 10.1713981,4.92890693 10.06,5.01 C9.96355413,5.07899707 9.84855493,5.11733013 9.73,5.12 C9.50294988,5.09989873 9.30778864,4.95080846 9.22869206,4.73703394 C9.14959549,4.52325941 9.20071421,4.28304556 9.36,4.12 C9.49556373,3.995926 9.64293112,3.88540047 9.8,3.79 C10.0677412,2.83288227 9.61394007,1.82106548 8.72111391,1.38446368 C7.82828776,0.947861878 6.75103191,1.21097499 6.16,2.01 L6.37,2.21 C6.5922265,2.44204201 6.5922265,2.80795799 6.37,3.04 C6.25749861,3.14167808 6.11163455,3.19860065 5.96,3.2 C5.80173844,3.19774577 5.65077828,3.13304856 5.54,3.02 C5.44920791,2.92077248 5.3406802,2.83937671 5.22,2.78 L5.15,2.78 C5.01929614,2.69125611 4.87361758,2.62688651 4.72,2.59 L4.65,2.32 L4.58,2.59 C4.22285427,2.59262541 3.88153447,2.73771852 3.63181951,2.99306614 C3.38210456,3.24841377 3.24465967,3.59288454 3.25,3.95 L3.25,4.07 L3.25,4.38 C3.26612637,4.452522 3.25165734,4.52848442 3.21,4.59 C3.16075276,4.64920184 3.08696992,4.68240412 3.01,4.68 L2.62,4.68 C2.00741211,4.70134235 1.46409352,5.07945126 1.23125157,5.64646452 C0.998409621,6.21347779 1.11920095,6.86430103 1.54,7.31 C1.82414581,7.61254659 2.21533275,7.79199014 2.63,7.81 L4.25,7.81 C4.54370895,7.84848267 4.76335145,8.09878072 4.76335145,8.395 C4.76335145,8.69121928 4.54370895,8.94151733 4.25,8.98 L2.62,8.98 C1.27558609,8.89009259 0.196070583,7.8360577 0.0740811957,6.49417444 C-0.0479081915,5.15229118 0.823838479,3.92086881 2.13,3.59 C2.13,3.59 2.13,3.41 2.13,3.41 L2.13,3.29 C2.13,3.29 2.19,3.1 2.21,3.06 L2.31,2.85 L2.36,2.75 L2.49,2.55 L2.63,2.37 L2.8,2.25 L2.87,2.17 L3.05,2.02 L3.24,1.88 L3.43,1.76 L3.65,1.66 L3.85,1.59 L4.1,1.53 L4.29,1.53 C4.38645965,1.52105307 4.48354035,1.52105307 4.58,1.53 L4.9,1.53 L5.1,1.53 C5.67999802,0.592727726 6.69790033,0.0159164184 7.8,0 C8.02467027,0.000101746779 8.24888652,0.0201808138 8.47,0.06 C10.1180201,0.387126569 11.242539,1.91977199 11.06,3.59 C12.4941341,3.70620199 13.5874519,4.9229011 13.5502302,6.36125365 C13.5130085,7.79960619 12.3582247,8.95812893 10.92,9 L9.8,8.98 Z" id="Path"></path>
                          </g>
                      </g>
                  </svg>
            <h2>
              {{CardData.Type}}</h2>
            <div v-for="(PolicyData, PolicyLabel) in CardData.policyData" :key="PolicyData.Policy" class="CardPolicyTextAll">
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
                <a href="#" :class="[CardData.ActionButton]">Invest Now</a>
              </div>
            </div>
            <div style="padding-top:40px">
              <a href="bondPolicyDetails" class="btn-primary">View Details</a>
            </div>
          </div>
        </div>
      </div>
      <div class="workAreaContent">
        <div class="MyTALCard">
          <h2>Can't find all your TAL products</h2>
          <p class="ActionText margin-top-30px">Click the add button to get started.
            <br> If you don't have your policy or investment number on hand please call 1300 209 088.</p>
          <div class="margin-top-30px"></div>
          <a href="#" class="btn-primary ">Add </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import myTALNav from '~/components/myTAL-Nav.vue'
  
  
  
  export default {
    components: {
      myTALNav
    },
    layout: 'AppView',
    data: function() {
      return {
  
        CardsInsurance: {
          Card1: {
            id: 1,
            Type: "Accelerated Protection",
            policyData: {
              "Policy Number": 22323223,
              "Sum insured": "$1,700,545.00",
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
            Type: "Sarah School fund",
            policyData: {
              "Account Number": 332323223,
              "Ballance": "$32,454.45",
              "Goal": "Education Savings",
              "Goal Amount" : "$1,243,3434.33",
              "Account Owner" : "Mr James Smith",
              "Lives insured" : "Sarah Smith",
              "Tax withdraw status": "unknown",
              "Current 10 year period end date" :  "10/1/2029",
            },
            Alert: "",
            AlertPrice: "",
            Action: "Your next investment will be on the 12/09/2019",
            ActionButton: "btn-primary-outline"
          },
        }
      }
    },
    methods: {
  
    }
  
  }
</script>

<style lang="scss" scoped>



.CardDataTextAll .CardPolicyTextAll:nth-child(4) .policyDataArea{
    font-size: 18px !important;
    font-weight:800;
}

  .margin-top-30px {
    padding-top: 30px
  }
  
  .MyTALCard {
    background-color: white;
    color: #222;
    flex: 1;
    padding: 30px;
    margin-top: 30px;
    margin-right: 30px;
    min-width: 520px;
  }
  
  .square {
    max-width: 520px;
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



</style>
