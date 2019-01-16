<template>
    <!--  <div id="app">
                <tree
                  :data="menuData"
                />
            
            -->
    <div style="background-color:red;">
        <h2>I would like to </h2>
    
        <div class="example-tree">
            <tree :data="menuData">
                <span class="tree-text" slot-scope="{ node }">
            
    
    <template>
        <a :href="node.data.link">
            <img :src="node.data.icon" alt="">
    <!--    <i :class="node.data.icon"></i> -->
        {{ node.text }}
        </a>
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
    .tree-arrow.has-child:after {
        border: 1.5px solid #494646;
        /* position: absolute; */
        border-left: 0;
        border-top: 0;
        left: 229px;
        margin-top: -6px;
        top: 50%;
        height: 9px;
        width: 9px;
        transform: rotateZ(45deg);
        transform-origin: center;
    }
    
    .tree-arrow.expanded.has-child:after {
        transform: rotateZ(225deg);
        transform-origin: center;
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
