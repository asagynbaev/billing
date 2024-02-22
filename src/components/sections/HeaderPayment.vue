<template>
    <header class="header-area navbar-light text-white fixed-top" :class="{'is-sticky': isSticky}">
        <div class="container-fluid container-fluid--cp-150">
            <nav class="navbar navbar-expand-lg" id="navbar-example2">
                <router-link to="/" class="navbar-brand logo-light">
                    <img src="../../assets/img/logo/logo.svg" alt="logo">
                </router-link>
                <router-link to="/" class="navbar-brand logo-dark">
                    <img src="../../assets/img/logo/logo-dark.png" alt="logo">
                </router-link>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>

                <div class="collapse navbar-collapse justify-content-center" id="navbarSupportedContent">
                    <ul class="nav main-menu">
                        <li class="nav-item">
                            <a class="nav-link" href="#home" @click="menuCollapseOnLinkClick">
                                <span>ГЛАВНАЯ</span>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#about" @click="menuCollapseOnLinkClick">
                                <span>О НАС</span>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#service" @click="menuCollapseOnLinkClick">
                                <span>СЕРВИСЫ</span>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#pricing" @click="menuCollapseOnLinkClick">
                                <span>ЦЕНЫ</span>
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#clients" @click="menuCollapseOnLinkClick">
                                <span>КЛИЕНТЫ</span>
                            </a>
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </header>
</template>

<script>
    export default {
        data (){
            return {
                isSticky: false
            }
        },
        mounted(){
            window.addEventListener('scroll', () => {
                let scroll = window.scrollY
                if(scroll >= 200){
                    this.isSticky = true
                } else {
                    this.isSticky = false
                }
            })
        },
        methods: {
            menuCollapseOnLinkClick() {
                document.getElementById('navbarSupportedContent').classList.remove('show')
            }
        },
    }
</script>