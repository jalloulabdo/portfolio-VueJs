<template>
        <section class="project section">
            <div class="project_bg">
                <div class="project_container container grid">
                    <div class="project_data">
                        <h2 class="project_title">You have new project</h2>
                        <p class="project_description">Contact me now </p>
                        <a href="#contact" class="button button--flex button--white">
                            Contact Me
                            <i class="uil uil-message project_icon button_icon"></i>
                        </a>
                    </div>
                    <div class="home_img project_img">
                        <img src="@/assets/images/home2.png" alt="">
                    </div>
                    <!-- <img src="@/assets/images/home2.png" alt="" class="project_img"> -->
                </div>
            </div>
        </section>
</template>

<script>
export default {
    name:'ProjectInMind'
}
</script>

<style>
.project_img {
    background-color: hsl(260deg 60% 99%) !important;
}
</style>