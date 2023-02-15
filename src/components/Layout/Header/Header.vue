<template>
    <header class="header" id="header">
        <nav class="nav container">
            <a href="#home" class="nav_logo">
                JALLOUL ABDERRAHIM
            </a>
    
            <div class="nav_menu" id="nav-menu" :class="{ show_menu: showMenuMobil === true}">
                <ul class="nav_list">
                    <li class="nav-item">
                        <a href="#home"  class="nav_link " @click="activenav = 'home'" :class="{ active_link: activenav === 'home'}">Home</a>
                    </li>
                    <li class="nav-item">
                        <a href="#about"  class="nav_link" @click="activenav = 'about'" :class="{ active_link: activenav === 'about'}">About</a>
                    </li>
                    <li class="nav-item">
                        <a href="#skills"  class="nav_link" @click="activenav = 'skills'" :class="{ active_link: activenav === 'skills'}">Skills</a>
                    </li>
                    <!-- <li class="nav-item">
                        <a href="#services"  class="nav_link" @click="activenav = 'services'" :class="{ active_link: activenav === 'services'}">Services</a>
                    </li> -->
                    <li class="nav-item">
                        <a href="#portfolio" class="nav_link" @click="activenav = 'portfolio'" :class="{ active_link: activenav === 'portfolio'}">Portfolio</a>
                    </li>
                    <li class="nav-item">
                        <a href="#contact"  class="nav_link" @click="activenav = 'contactme'" :class="{ active_link: activenav === 'contactme'}">Contact Me</a>
                    </li>
                </ul>
    
                <div class="nav_close" id="nav-close">
                    <i class="uil uil-times nav_close" id="nav-close" @click="closemenuButton()"></i>
                </div>
            </div>
    
            <div class="nav_btns">
                <!--===== THEME CHANGE BUTTON =====-->
                <i class="uil uil-moon change_theme" :class="isnight ? 'uil-sun' : 'uil-moon'"
                    @click="functionButton(this)"></i>
    
                <div class="nav_toogle" id="nav-toggle">
                    <i class="uil uil-bars"  @click="menuButton()"></i>
                </div>
            </div>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaDer',
    data() {
        return {
            darkTheme : 'dark-theme',
            iconTheme : 'uil-sun',
            isnight : false,
            selectedTheme : '' ,
            selectedIcon: '',
            activenav: 'home',
            scrollY: window.pageYOffset,
            showMenuMobil: false
        }
    },
    methods: {
        functionButton() {

            document.body.classList.toggle(this.darkTheme)
            this.isnight = !this.isnight
            localStorage.setItem('selected-theme', document.body.classList.contains(this.darkTheme) ? 'dark' : 'light')
            this.selectedTheme = localStorage.getItem('selected-theme')
            document.body.classList[this.selectedTheme === 'dark' ? 'add' : 'remove'](this.darkTheme)

        },
        menuButton(){
           this.showMenuMobil = !this.showMenuMobil
        },
        closemenuButton(){
            this.showMenuMobil = !this.showMenuMobil
        }
    
    }
}
</script>