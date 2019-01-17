<template>
    <div>
        <div class="example-tree">
            <tree :data="menuData">
                <span class="tree-text" slot-scope="{ node }">
        <template>
            <div>
            <a class="Navigation" :href="node.data.link"> 
              <div class="icon-menu">  <img  :src="node.data.icon" alt="" width="18px"> </div>
           <div class="navText" >{{ node.text }}</div> 
            </a>
            </div>
    </template>
            </span>
          </tree>
        </div>

  </div>


</template>

<script>
    export default {
        data: function() {
            return {
                menuData: [
                     {
                        text: 'Accelerated Protection',
                        data: {
                            icon: 'Life-white-4.svg',
                        },
                        state: {
                            expanded: false
                        },
                        children: [{
                                text: '- Accelerated Protection - 1665317',
                                data: {
                                    icon: '',
                                    link: 'Testpage'
                                }
                            },
                            {
                                text: '- Accelerated Protection - 1666140',
                                data: {
                                    icon: '',
                                    link: 'Testpage'
                                }
                            },

                    {
                        text: 'Request a Statement',
                        data: {
                            icon: '.request-statement-0.svg',
                            link: 'Testpage'
                        }
    
                    },
                    {
                        text: 'Request a Certificate of Currency',
                        data: {
                            icon: '.request-CC-0.svg',
                            link: 'Testpage'
                        }
    
                    },
                        ]
                    },{
                        text: 'Smart Wealth',
                        data: {
                            icon: 'SWealth-white-04.svg',
                        },
                        state: {
                            expanded: false
                        },
                        children: [{
                                text: '- Smart Wealth - 1665317',
                                data: {
                                    icon: '',
                                    link: 'bondPolicyDetails'
                                }
                            },
                           
                        ]
                    },
    
              
                    
                    {
                        text: 'Overdue payments',
                        data: {
                            icon: '/overdue-payments-0.svg',
                            link: 'Testpage'
                        }
    
                    },
                     {
                        text: 'Add Policy / Investment',
                        data: {
                            icon: '/add-policy-0.svg',
                            link: 'Testpage'
                        }
    
                    },
                   
                
                    {
                        text: 'Change Password',
                        data: {
                            icon: '/change-password-0.svg',
                            link: 'Testpage'
                        }
    
                    },
                ]
    
            }
        }
    }
</script>

<style>





    .StartNavText {
        color: #fff !important !important;
        font-size: 15px !important !important;
        font-size: .9375rem !important !important;
        margin-bottom: 25px !important !important;
        margin-top: 20px !important !important;
        line-height: 1.33 !important !important;
        letter-spacing: inherit !important !important;
        font-weight: 700 !important !important;
    }
    
    .Navigation {
        color: white !important;
        font-size: .8125rem !important;
        line-height: 1.1538461538 !important;
        font-weight: 500 !important;
        transition-duration: 250ms !important;
    }
    
    .example-tree {
        margin-left: -43px !important;
        max-width: 270px !important !important;
    }
    
    .navText {
        margin-left: 30px !important;
        white-space: normal !important;
         transition-duration: 250ms !important;
    }
    
    .navText:hover {
        margin-left: 30px !important;
        white-space: normal !important;
        color: #80C342 !important;
    }
    
    .icon-menu {
        float: left
    }
    
    .tree-children .tree-node .tree-content .tree-anchor {
        border-bottom: 1px solid transparent !important;
        margin-left: -50px !important;
      
    }


    .tree-children  .tree-node {
       background-color: #35434b !important;
       margin-left:33px !important;
       margin-top:-3px !important;
    }

    .tree > .tree-root{
         margin-right: 27px;
    }
    
    .tree-root .tree-node .tree-content .tree-anchor {
        border-bottom: 1px solid  #35434b !important;
        padding-top: 10px !important;
        padding-bottom: 10px !important;
        white-space: normal !important;
    }
    
    .tree-node {
        white-space: normal !important;
    }
    
    .tree-arrow.has-child:after {
        border: 1px solid white !important;
        /* position: absolute !important; */
        border-left: 0 !important;
        border-top: 0 !important;
        left: 235px !important;
        top: 50% !important;
        height: 9px !important;
        width: 9px !important;
        transform: rotateZ(45deg) !important;
        transform-origin: center !important;
        margin-top: -8px !important;
    }
    
    .tree-arrow.expanded.has-child:after {
        border: 1px solid #80C342 !important;
        /* position: absolute !important; */
        border-left: 0 !important;
        border-top: 0 !important;
        left: 235px !important;
        top: 50% !important;
        height: 9px !important;
        width: 9px !important;
        transform: rotateZ(225deg) !important;
        transform-origin: center !important;
        margin-top: -8px !important;
    }
    
    .tree-node.selected>.tree-content {
        background-color: transparent !important;
    }
    
    .tree-node:not(.selected)>.tree-content:hover {
        background: transparent !important;
    }
    
    .l-fade-enter-active,
    .l-fade-leave-active {
        transition: opacity .3s, transform .3s !important;
        transform: translateY(0) !important;
    }
    
    .l-fade-enter,
    .l-fade-leave-to {
        opacity: 0 !important;
        transform: translateY(-0.1em) !important;
    }
</style>
