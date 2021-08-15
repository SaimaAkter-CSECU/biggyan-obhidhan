<template>
    <div class="banner mt-5">
        <div class="container">
            <div class="row d-flex align-items-center">
                <div class="col-md-6 col-sm-12">
                    <h1 class="banner-header mb-3">বাংলা ভাষায় বিশ্বে প্রথম পূর্ণাঙ্গ বিজ্ঞান অভিধান</h1>
                    <div class="banner-text mt-5">বিজ্ঞানকে ভয় নয়,</div>
                    <div class="banner-text">সবাই মিলে করব জয়</div>
                    <div class="banner-btn mt-4">
                        <a href="#">
                            <img :src="bannerGplay" class="img-fluid" alt="">
                        </a>
                    </div> 
                </div>
                <div class="col-md-6 col-sm-12">
                    <img :src="banner" class="img-fluid" alt="Biggyan Obhidhan">
                </div>
            </div>
        </div>        
    </div>
</template>

<script>
    import banner from '../assets/banner-img.png'
    import bannerGplay from '../assets/google-play-btn-banner.png'
    export default {
        name: "BannerSection",
        data : () => ({
            banner: banner,
            bannerGplay: bannerGplay
        }),
    }
</script>