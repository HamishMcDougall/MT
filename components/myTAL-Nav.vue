<template>
    <div>
        <div class="example-tree" >
            <tree :data="menuData" >
                <span class="tree-text" slot-scope="{ node }" :class='[node.data.class]'>
        <template>
            <div >
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
                             class: 'topLevel'
                        },
                        state: {
                            expanded: false
                        },
                        children: [{
                                text: '- Accelerated Protection - 1665317',
                                data: {
                                    icon: '',
                                    link: 'Testpage',
                                    class: 'subNav'
                                }
                            },
                            {
                                text: '- Accelerated Protection - 1666140',
                                data: {
                                    icon: '',
                                    link: 'Testpage',
                                     class: 'subNav'
                                }
                            },

                    {
                        text: 'Request a Statement',
                        data: {
                            icon: '',
                            link: 'Testpage',
                            class: 'subNav'
                        }
    
                    },
                    {
                        text: 'Request a Certificate of Currency',
                        data: {
                            icon: '',
                            link: 'Testpage',
                            class: 'subNav'
                        }
    
                    },
                        {
                        text: 'Overdue payments',
                        data: {
                            icon: '',
                            link: 'Testpage',
                            class: 'subNav'
                        }
    
                    },
                        ]
                    },{
                        text: 'Smart Wealth',
                        data: {
                            icon: 'SWealth-white-04.svg',
                            class:'topLevel'
                        },
                        state: {
                            expanded: false
                        },
                        children: [{
                                text: '- Sarah School Fund',
                                data: {
                                    icon: '',
                                    link: 'bondPolicyDetails',
                                    class: 'subNav'
                                }
                            },
                           
                        ]
                    },
    
              
                    
                 
                     {
                        text: 'Add Policy / Investment',
                        data: {
                            icon: '',
                            link: 'Testpage',
                            class: 'Utility , Utility-top'
                        }
    
                    },
                   
                
                    {
                        text: 'Change Password',
                        data: {
                            icon: '',
                            link: 'Testpage',
                            class: 'Utility'
                        }
    
                    },
                ]
    
            }
        }
    }
</script>

<style lang="scss">

 .tree-anchor {
   padding-left: 0px !important;
 }




    .StartNavText {
        color: #fff !important ;
        font-size: 15px !important ;
        font-size: .9375rem !important ;
        margin-bottom: 25px !important ;
        margin-top: 20px !important ;
        line-height: 1.33 !important ;
        letter-spacing: inherit !important ;
        font-weight: 700 !important ;
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
        max-width: 270px !important ;
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
        margin-left: -50px !important;
      
    }


    .tree-children  .tree-node {
       background-color: #35434b !important;
       margin-left:33px !important;
       margin-top:-6px !important;
       padding-top:10px;
       width:220px !important;
    }

    .tree > .tree-root{
         margin-right: 27px;
    }
    
    .tree-root .tree-node .tree-content .tree-anchor {
      
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
        border: 1px solid $Primary-LightGreen !important;
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

    .topLevel{
        border-bottom: 1px solid  #35434b !important;
        padding-top: 10px !important;
        padding-bottom: 10px !important;
        white-space: normal !important;
        width:220px;
    }

    .Utility-top {
        margin-top:30px;
    }

    .Utility{
        margin-left: -25px;
    }

    .subNav{
       width:220px;
        padding-bottom: 10px;
    }

   
  
</style>
