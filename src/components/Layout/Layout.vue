<template>
    <Header />
    <main class="main">
        <Home />
        <About />
        <Skills />
        <Qualification />
        <Services />
        <Portfolio />
        <ProjectInMind />
        <ContactMe />
    </main>
    <Footer />
</template>

<script>
import Header from './Header/Header'
import Footer from './Footer/Footer'
import Home from './Content/Home'
import About from './Content/About'
import Skills from './Content/Skills'
import Qualification from './Content/Qualification'
import Services from './Content/Services'
import Portfolio from './Content/Portfolio'
import ProjectInMind from './Content/Projectinmind'
import ContactMe from './Content/ContactMe'


export default {
    
    name:'LaYout',
    components: {
        Header,
        Footer,
        Home,
        About,
        Skills,
        Qualification,
        Services,
        Portfolio,
        ProjectInMind,
        ContactMe
    }
}
</script>