<template>
    <section class="skills section" id="skills">
        <h2 class="section__title">Skills</h2>
        <span class="section__subtitle">My technical lever</span>
    
        <div class="skills_container container grid">
            <div>
                <!--=========== SKILL 1 ============-->
                <div class="skills_content " :class="first ? 'skills_open' : 'skills_close'">
                    <div class="skills_header">
                        <i class="uil uil-brackets-curly skills_icon"></i>
    
                        <div>
                            <h1 class="skills_title">Frontend developer</h1>
                        </div>
    
                        <i class="uil uil-angle-down skills_arrow" @click="firstSkill()"></i>
                    </div>
                    <div class="skills_list grid">
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">HTML</h3>
                                <span class="skills_number">95%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_html"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">SASS</h3>
                                <span class="skills_number">80%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_css"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">JAVASCRIPT</h3>
                                <span class="skills_number">80%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_javascript"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">Vue js</h3>
                                <span class="skills_number">70%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_vuejs"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">nuxt js</h3>
                                <span class="skills_number">70%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_vuejs"></span>
                            </div>
                        </div>
                    </div>
                </div>
                <!--=========== SKILL 2 ============-->
                <div class="skills_content " :class="secnd ? 'skills_open' : 'skills_close'">
                    <div class="skills_header">
                        <i class="uil uil-server-network skills_icon"></i>
    
                        <div>
                            <h1 class="skills_title">Backend developer</h1>
                        </div>
    
                        <i class="uil uil-angle-down skills_arrow" @click="secndSkill()"></i>
                    </div>
                    <div class="skills_list grid">
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">PHP</h3>
                                <span class="skills_number">80%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_php"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">Laravel</h3>
                                <span class="skills_number">80%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_php"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">Node JS</h3>
                                <span class="skills_number">50%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_nodejs"></span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div>
                <!--=========== SKILL 3 ============-->
                <div class="skills_content " :class="last ? 'skills_open' : 'skills_close'">
                    <div class="skills_header">
                        <i class="uil uil-server-network skills_icon"></i>
    
                        <div>
                            <h1 class="skills_title">Designer</h1>
                            <span class="skills_subtitle"></span>
                        </div>
    
                        <i class="uil uil-angle-down skills_arrow" @click="lastSkill()"></i>
                    </div>
                    <div class="skills_list grid">
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">Figma</h3>
                                <span class="skills_number">50%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_figma"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">Photoshop</h3>
                                <span class="skills_number">45%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_nodejs"></span>
                            </div>
                        </div>
                        <div class="skills_data">
                            <div class="skills_titles">
                                <h3 class="skills_name">Illustrator</h3>
                                <span class="skills_number">85%</span>
                            </div>
                            <div class="skills_bar">
                                <span class="skills_percentage skills_photoshop"></span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SkiLLs',
    data() {
        return {
            first: true,
            secnd: true,
            last:true
        }
    },
    methods: {
         firstSkill() {
            this.first = !this.first
        },
        secndSkill () {
            this.secnd = !this.secnd
        },
        lastSkill () {
            this.last = !this.last
        }
    }
}
</script>