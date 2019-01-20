<template>
    <div>
        <div class="Grid">
            <div class="topBar">
                <div class="phoneText">1300 209 088</div>
                <div class="UserEmail">XDDESIGN@GMAIL.COM</div>
                <a href="#">
                    <div class="LogOutButton"> LOG OUT </div>
                </a>
            </div>
            <div class="navigationDesktop">
                <div>
                    <a href="dashboard"><img src="~/assets/logo-primary.svg" alt="TAL"></a>
                </div>
                <div class="myTALtext">myTAL</div>
                <a href="#">
                    <div class="link helpBtn">Help</div>
                </a>
            </div>
    
    
    
            <nuxt/>
    
    
            <div class="footer">
                <footer class="footer-global">
                    <div class="p-footer-container">
                        <div class="c-logo">
                            <img src="~/assets/logo-primary.svg" alt="TAL">
                        </div>
                        <div class="footer-text">
                            <div class="footer-links">
                                <div class="site-link">
                                    About
                                </div>
                                <div class="site-link">
                                    Contact
                                </div>
                                <div class="site-link">
                                    Privacy
                                </div>
                            </div>
    
                            <div class="rte">
                                <p class="small">2012-2015 © TAL Services Limited ABN 60 076 105 130 a Dai-ichi Life Group Company</p>
                            </div>
                        </div>
                    </div>
                </footer>
            </div>
    
        </div>
    
    
    
    
    </div>
</template>




<style>
    html {
        font-family: "Pluto Sans", Arial, Helvetica, sans-serif;
        height: 100%;
    }
    
    body {
        min-height: 100%;
    }
    
    *,
    *:before,
    *:after {
        box-sizing: border-box;
        margin: 0;
    }
    
    .footer-global {
        background-color: rgb(26, 30, 33);
        height: 235px;
        padding-left: 60px;
        padding-right: 60px;
        padding-top: 40px;
    }
    
    .c-logo {
        margin-top: 50px;
        padding-right: 20px;
    }
    
    .footer-text {
        max-width: 1200px;
        color: #AAACAE;
        font-size: 11px;
        padding-left: 205px;
        margin-top: -20px;
    }
    
    .footer-links {
        display: flex;
        flex-direction: row;
        padding-bottom: 20px;
    }
    
    .site-link {
        display: block;
        position: relative;
        color: #fff;
        text-decoration: none;
        font-weight: 700;
        border-bottom: 1px solid #303E46;
        transition: all 0.1s ease-out;
        padding-bottom: 6px;
        margin-right: 30px;
        font-size: 13px;
        width: 210px;
    }
    
    .site-link:hover {
        border-bottom: 1px solid #80C342;
        cursor: pointer;
    }
    
    .small {
        padding-bottom: 20px;
    }
</style>
