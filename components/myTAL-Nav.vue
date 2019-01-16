<template>

    <div>
        <div class="StartNavText">I would like to: </div>
    
        <div class="example-tree">
            <tree :data="menuData">
                <span class="tree-text" slot-scope="{ node }">
            
    
    <template>
        <div>
        <a class="Navigation" :href="node.data.link"> 
          <div class="icon-menu">  <img  :src="node.data.icon" alt=""> </div>
    <!--    <i :class="node.data.icon"></i> -->
       <div class="navText" >{{ node.text }}</div> 
        </a>
        </div>
</template>
            </span>
          </tree>
        </div>

  </div>
</div>

</template>

<script>
    export default {
        data: function() {
            return {
                menuData: [{
                        text: 'View Policy Details',
                        data: {
                            icon: '/view-policy-details.svg',
                        },
                        state: {
                            expanded: false
                        },
                        children: [{
                                text: '- Accelerated Protection - 1665317',
                                data: {
                                    icon: '',
                                    link: '/index.html'
                                }
                            },
                            {
                                text: '- Accelerated Protection - 1666140',
                                data: {
                                    icon: '',
                                    link: '/index.html'
                                }
                            },
                        ]
                    },
    
                    {
                        text: 'Request a Statement',
                        data: {
                            icon: '/request-statement.svg',
                            link: '/index.html'
                        }
    
                    },
                    {
                        text: 'Request a Certificate of Currency',
                        data: {
                            icon: '/request-CC.svg',
                            link: '/index.html'
                        }
    
                    },
                    {
                        text: 'Add Policy',
                        data: {
                            icon: '/add-policy.svg',
                            link: '/index.html'
                        }
    
                    },
                    {
                        text: 'Change Password',
                        data: {
                            icon: '/change-password.svg',
                            link: '/index.html'
                        }
    
                    },
                    {
                        text: 'Overdue payments',
                        data: {
                            icon: '/overdue-payments.svg',
                            link: '/index.html'
                        }
    
                    },
                    {
                        text: '- Accelerated Protection - 1666140',
                        data: {
                            icon: '',
                            link: '/index.html'
                        }
    
                    }
                ]
    
            }
        }
    }
</script>

<style>

.StartNavText{
    color: #fff;
    font-size: 15px;
    font-size: .9375rem;
    margin-bottom: 25px;
    margin-top: 20px;
    line-height: 1.33;
    letter-spacing: inherit;
    font-weight: 700;
}

.Navigation{
    color:white;
    font-size: .8125rem;
    line-height: 1.1538461538;
    font-weight: 500;
    transition-duration: 250ms;
}

.example-tree{
    margin-left: -43px;
    max-width: 270px !important;
}

.navText{
      margin-left:30px;
    white-space:normal;
      
}

.navText:hover{
      margin-left:30px;
    white-space:normal;
    color: #80C342;
      
}

.icon-menu{
        float: left
}

.tree-children .tree-node .tree-content .tree-anchor {
     border-top: 1px solid transparent !important;
     margin-left:-20px;
}

.tree-root .tree-node .tree-content .tree-anchor{
     border-top: 1px solid rgba(255,255,255,0.1);
      padding-top: 17px;
      margin-bottom: 5px;
      white-space:normal;
}

.tree-node {
    white-space:normal;
       
  
    }
    .tree-arrow.has-child:after {
        border: 1px solid white;
        /* position: absolute; */
        border-left: 0;
        border-top: 0;
        left: 229px;
        top: 50%;
        height: 9px;
        width: 9px;
        transform: rotateZ(45deg);
        transform-origin: center;
        margin-top: -3px;
    }
    
    .tree-arrow.expanded.has-child:after {
        border: 1px solid #80C342;
        /* position: absolute; */
        border-left: 0;
        border-top: 0;
        left: 229px;
        top: 50%;
        height: 9px;
        width: 9px;
 
        transform: rotateZ(225deg);
        transform-origin: center;
        margin-top: 3px;
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
       transform: translateY(-0.5em);
    }
</style>
