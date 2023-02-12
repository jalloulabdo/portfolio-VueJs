<template>
    <header class="header" id="header">
        <nav class="nav container">
            <a href="#home" class="nav_logo">
                JALLOUL ABDERRAHIM
            </a>
    
            <div class="nav_menu" id="nav-menu">
                <ul class="nav_list">
                    <li class="nav-item">
                        <a href="#home"  class="nav_link " @click="showMobileMenu = 'home'" :class="{ active_link: showMobileMenu === 'home'}">Home</a>
                    </li>
                    <li class="nav-item">
                        <a href="#about"  class="nav_link" @click="showMobileMenu = 'about'" :class="{ active_link: showMobileMenu === 'about'}">About</a>
                    </li>
                    <li class="nav-item">
                        <a href="#skills"  class="nav_link" @click="showMobileMenu = 'skills'" :class="{ active_link: showMobileMenu === 'skills'}">Skills</a>
                    </li>
                    <li class="nav-item">
                        <a href="#services"  class="nav_link" @click="showMobileMenu = 'services'" :class="{ active_link: showMobileMenu === 'services'}">Services</a>
                    </li>
                    <li class="nav-item">
                        <a href="#portfolio" class="nav_link" @click="showMobileMenu = 'portfolio'" :class="{ active_link: showMobileMenu === 'portfolio'}">Portfolio</a>
                    </li>
                    <li class="nav-item">
                        <a href="#contact"  class="nav_link" @click="showMobileMenu = 'contactme'" :class="{ active_link: showMobileMenu === 'contactme'}">Contact Me</a>
                    </li>
                </ul>
    
                <div class="nav_close" id="nav-close">
                    <i class="uil uil-times nav_close" id="nav-close"></i>
                </div>
            </div>
    
            <div class="nav_btns">
                <!--===== THEME CHANGE BUTTON =====-->
                <i class="uil uil-moon change_theme" :class="isnight ? 'uil-sun' : 'uil-moon'"
                    @click="functionButton(this)"></i>
    
                <div class="nav_toogle" id="nav-toggle">
                    <i class="uil uil-bars"></i>
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
            showMobileMenu: 'home',
            scrollY: window.pageYOffset,
             
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
    
    }
}
</script>