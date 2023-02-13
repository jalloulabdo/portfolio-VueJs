<template>
    <section class="contact section" id="contact">
        <h2 class="section__title">Contact Me</h2>
        <span class="section__subtitle">Get in touch</span>
    
        <div class="contact_container container grid">
            <div>
                <div class="contact_information">
                    <i class="uil uil-phone contact_icon"></i>
    
                    <div>
                        <h3 class="contact_title">Call Me</h3>
                        <span class="contact_subtitle">06 41 68 78 53</span>
                    </div>
                </div>
                <div class="contact_information">
                    <i class="uil uil-envelope contact_icon"></i>
    
                    <div>
                        <h3 class="contact_title">Email</h3>
                        <span class="contact_subtitle">jalloulabdo88@gmail.com</span>
                    </div>
                </div>
                <div class="contact_information">
                    <i class="uil uil-map-marker contact_icon"></i>
    
                    <div>
                        <h3 class="contact_title">Location</h3>
                        <span class="contact_subtitle">Lot Masoudi N 14 Drarga Agadir </span>
                    </div>
                </div>
            </div>
    
            <form @submit.prevent="sendMail">
                <div class="contact_inputs grid">
                    <div class="contact_content">
                        <label for="" class="contact_label">Name</label>
                        <input type="text" class="contact_input" name="name" id="name" v-model="form.name">
                        
                    </div>
                    <div class="contact_content">
                        <label for="" class="contact_label">Email</label>
                        <input type="email" name="email" id="email" class="contact_input" v-model="form.email">
                        
                    </div>
                    <div class="contact_content">
                        <label for="" class="contact_label">Message</label>
                        <textarea cols="0" rows="7" class="contact_input" id="message" name="message"
                           v-model="form.message"></textarea>
                        
                    </div>
                </div>
    
                <div class="" style="float: right;margin-top: 12px;">
                    <button type="submit" class="button button--flex" style="border: none;">
                        Send Message
                        <i class="uil uil-message button_icon"></i>
                    </button>
                </div>
            </form>
        </div>
    </section>
</template>
<script>
import emailjs from 'emailjs-com';


export default {

    data() {
        return {
            form: {
                email: '',
                name: '',
                message:''
            },
            inputFieldReset:null
        }
    },
    methods: {
        sendMail(e) {
            emailjs.sendForm('service_ca3rb5j', 'template_ehku7ip', e.target, 'tMAmKrtykuQmkLmSq', {
                name: this.form.name,
                email: this.form.email,
                message: this.form.message
            })
                .then(() => {
                    this.inputFieldReset = " ";
                    this.form.name = "";
                    this.form.email = "";
                    this.form.message = "";
                    this.$swal({
                        position: 'top-end',
                        icon: 'success',
                        title: 'Your message is send successful',
                        showConfirmButton: false,
                        timer: 1500
                    })
                }, (error) => {
                    alert('Message not sent', error);
                });
        }
    }
    

}

</script>