<template>
    <footer class="text-white" id="contact">
        <div class="footer-menu py-3">
            <div class="container">
                <div class="row">
                    <div class="col-md-3 col-sm-12 my-3 text-center">
                        <div class="footer-menu-logo">
                            <img :src="logo" class="img-fluid" alt="">
                        </div>
                        <div class="footer-menu-text my-3">
                            <p>বাংলা ভাষাভাষীদের জন্য প্রথম পূর্ণাঙ্গ বিজ্ঞান অভিধান মোবাইল অ্যাপ</p>
                        </div>
                        <div class="footer-menu-social-icon mb-5 d-flex justify-content-center">
                            <a href="https://m.me/bigganovidhan" class="me-2 social-icon">
                                <i class="fab fa-facebook-f text-hover d-flex align-items-center justify-content-center"></i>
                            </a>
                            <a href="https://m.me/bigganovidhan" class="me-2 social-icon">
                                <i class="fab fa-facebook-messenger text-hover d-flex align-items-center justify-content-center"></i>
                            </a>
                            <a href="https://wa.me/+8801646663999" class="me-2 social-icon">
                                <i class="fab fa-whatsapp text-hover d-flex align-items-center justify-content-center"></i>
                            </a>
                        </div>
                    </div>
                    <div class="col-md-1 d-md-block d-sm-none"></div>
                    <div class="col-md-4 col-sm-12 my-3">
                        <div class="footer-menu-header py-3">
                            <h5>Contact Info</h5>
                        </div>
                        <div class="footer-menu-list py-2">
                            <p class="mb-3">
                                <a href="https://www.google.com/maps/place/bti+Central+Plaza,+Green+Rd,+Dhaka+1215/@23.7572908,90.3874542,17z/data=!3m1!4b1!4m5!3m4!1s0x3755b8a15a64a9c1:0xa0392de87f2aceae!8m2!3d23.7572859!4d90.3896429" class="text-hover d-flex align-items-center">
                                    <span class="material-icons-outlined me-3">room</span>
                                    <span>BTI Central Plaza, Farmgate </span>
                                </a>
                            </p>
                            <p class="mb-3">
                                <a href="https://www.google.com/maps/place/bti+Central+Plaza,+Green+Rd,+Dhaka+1215/@23.7572908,90.3874542,17z/data=!3m1!4b1!4m5!3m4!1s0x3755b8a15a64a9c1:0xa0392de87f2aceae!8m2!3d23.7572859!4d90.3896429" class="text-hover d-flex align-items-center">
                                    <span class="material-icons-outlined me-3">push_pin</span>
                                    <span>Dhaka </span>
                                </a>
                            </p>
                            <p class="mb-3">
                                <a href="mailto:xyz@gmail.com" class="text-hover d-flex align-items-center">
                                    <span class="material-icons-outlined me-3">email</span>
                                    <span>xyz@gmail.com</span>
                                </a>
                            </p>
                            <p>
                                <a href="callto:+8801646663999" class="text-hover d-flex align-items-center">
                                    <span class="material-icons-outlined me-3">call</span>
                                    <span>+8801646663999 </span>
                                </a>
                            </p>
                        </div>
                    </div>
                    <div class="col-md-1 d-md-block d-sm-none"></div>
                    <div class="col-md-3 col-sm-12 my-3">
                        <div class="footer-menu-header py-3">
                            <h5>Support &amp; Download</h5>
                        </div>
                        <div class="footer-menu-list py-2">
                            <p>প্লেস্টোর থেকে এখনই ডাউনলোড করুন Biggan Ovidhan মোবাইল অ্যাপ</p>
                            <div class="mt-5">
                                <a href="http://play.google.com">
                                    <img :src="googlePlay" class="img-fluid" alt="">
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-credit">
            <div class="container d-flex justify-content-center py-4">
                <small class="m-0 px-3"> &copy; Copyright <a href="#" class="text-hover"><strong>Nextive Group</strong></a> । Developed By <a href="#" class="text-hover"><strong>Nextive Solution</strong></a> </small>
            </div>
        </div>
        <a href="#" class="back-to-top text-white" v-bind:class=" (scrollPosition < 120)? 'd-none': '' ">
            <span class="material-icons-outlined w-100 h-100 d-flex justify-content-center align-items-center">north</span>
        </a>
    </footer>
</template>

<script>
    import '../css/style.css'; 
    import logo from '../assets/biggyan-logo.png'
    import googlePlay from '../assets/google-play-btn.png'
  
    export default {
        name: 'FooterSection',
        // data(){
        //     return{
        //         logo: logo
        //     }
        // }, 
        data: () => ({
            logo: logo,
            googlePlay : googlePlay, 
            scrollPosition: null
        }),
        methods: {
            updateScroll() {
                this.scrollPosition = window.scrollY;
            },
        },
        mounted() {
            window.addEventListener("scroll", this.updateScroll);
        },
    }
</script>
