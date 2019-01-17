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
                                    link: 'Testpage'
                                }
                            },
                            {
                                text: '- Smart Wealth - 1666140',
                                data: {
                                    icon: '',
                                    link: 'Testpage'
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
        color: #fff;
        font-size: 15px;
        font-size: .9375rem;
        margin-bottom: 25px;
        margin-top: 20px;
        line-height: 1.33;
        letter-spacing: inherit;
        font-weight: 700;
    }
    
    .Navigation {
        color: white;
        font-size: .8125rem;
        line-height: 1.1538461538;
        font-weight: 500;
        transition-duration: 250ms;
    }
    
    .example-tree {
        margin-left: -43px;
        max-width: 270px !important;
    }
    
    .navText {
        margin-left: 30px;
        white-space: normal;
         transition-duration: 250ms;
    }
    
    .navText:hover {
        margin-left: 30px;
        white-space: normal;
        color: #80C342;
    }
    
    .icon-menu {
        float: left
    }
    
    .tree-children .tree-node .tree-content .tree-anchor {
        border-bottom: 1px solid transparent !important;
        margin-left: -50px;
      
    }


    .tree-children  .tree-node {
       background-color: #35434b;
       margin-left:33px;
       margin-top:-3px;
    }
    
    .tree-root .tree-node .tree-content .tree-anchor {
        border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        padding-top: 10px;
        padding-bottom: 10px;
        white-space: normal;
    }
    
    .tree-node {
        white-space: normal;
    }
    
    .tree-arrow.has-child:after {
        border: 1px solid white;
        /* position: absolute; */
        border-left: 0;
        border-top: 0;
        left: 235px;
        top: 50%;
        height: 9px;
        width: 9px;
        transform: rotateZ(45deg);
        transform-origin: center;
        margin-top: -8px;
    }
    
    .tree-arrow.expanded.has-child:after {
        border: 1px solid #80C342;
        /* position: absolute; */
        border-left: 0;
        border-top: 0;
        left: 235px;
        top: 50%;
        height: 9px;
        width: 9px;
        transform: rotateZ(225deg);
        transform-origin: center;
        margin-top: -8px;
    }
    
    .tree-node.selected>.tree-content {
        background-color: transparent;
    }
    
    .tree-node:not(.selected)>.tree-content:hover {
        background: transparent;
    }
    
    .l-fade-enter-active,
    .l-fade-leave-active {
        transition: opacity .3s, transform .3s;
        transform: translateY(0);
    }
    
    .l-fade-enter,
    .l-fade-leave-to {
        opacity: 0;
        transform: translateY(-0.1em);
    }
</style>
