<template>
    <section id="service">
        <div class="container section-content py-5">
            <div class="row d-flex align-items-center">
                <div class="col-md-4 col-sm-12 text-end">
                    <div class="card-div bg-transparent py-4">
                        <h4 class="card-title mb-3 text-hover">
                            <span @click="changeImage(1)" class="">দশ হাজার বিজ্ঞান শব্দকোষ</span>
                        </h4>
                        <p class="card-text">৫ম থেকে ১২শ ক্লাস পর্যন্ত শিক্ষার্থীদের প্রয়োজনীয় সকল বিজ্ঞান রিলেটেড কিওয়ার্ড।</p> 
                    </div>
                    <div class="card-div bg-transparent py-4">
                        <h4 class="card-title mb-3">
                            <span @click="changeImage(2)" class="text-hover">গেইমিং</span>
                        </h4>
                        <p class="card-text">খেলার ছলে বিজ্ঞান কে বুঝার জন্য রয়েছে বিভিন্ন গেইমিং সুবিধা</p> 
                    </div>
                    <div class="card-div bg-transparent py-4">
                        <h4 class="card-title mb-3">
                            <span @click="changeImage(3)" class="text-hover">কন্ট্রিবিউশন</span>
                        </h4>
                        <p class="card-text">শিক্ষার্থীদের জন্য প্রয়োজনীয় শব্দ কন্ট্রিবিউট করে সমৃদ্ধ করতে পারবে আমাদের শব্দভান্ডার</p> 
                    </div>
                </div>
                <div class="col-md-4 col-sm-12 d-md-block d-sm-none">
                    <div class="service-img text-center py-3">
                        <img :src="serviceImg" class="img-fluid service-img" alt=""> 
                    </div>
                </div>
                <div class="col-md-4 col-sm-12 text-left">
                    <div class="card-div bg-transparent py-5">
                        <h4 class="card-title mb-3">
                            <span @click="changeImage(4)" class="text-hover">ইন্টারেক্টিভ কনটেন্ট</span>
                        </h4>
                        <p class="card-text">প্রতিটি টপিক কে সুন্দর ভাবে ফুটিয়ে তুলতে গ্রাফ,চার্ট,লেখচিত্রের পাশাপাশি রয়েছে এনিমেটেড কন্টেন্ট</p> 
                    </div>
                    <div class="card-div bg-transparent py-4">
                        <h4 class="card-title mb-3">
                            <span @click="changeImage(5)" class="text-hover">এআই বেইজড লারনিং</span>
                        </h4>
                        <p class="card-text">শিক্ষার্থীদের মনোযোগ ধরে রাখতে এবং শেখার আগ্রহ বাড়াতে ব্যবহার করা হয়েছে আর্টিফিশিয়াল ইন্টিলিজেন্স টেকনোলজি</p> 
                    </div>
                    <div class="card-div bg-transparent py-4">
                        <h4 class="card-title mb-3">
                            <span @click="changeImage(6)" class="text-hover">ইউজার কমিউনিটি</span>
                        </h4>
                        <p class="card-text">দেশের বৃহত্তম বিজ্ঞানপ্রেমী কমিউনিটি শিক্ষার্থীদের জানার আগ্রহ এবং কম্পিটিটিভ স্কিল বাড়াবে</p> 
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    // import serviceImg from '../assets/service.jpg' 

    export default{
        name: 'ServiceSection',
        data : () => ({
            serviceImg: require('../assets/service/service.jpg'),
            imgStore: [
                {
                    id: 1, 
                    img_src: require('../assets/service/service1.jpg'), 
                },
                {
                    id: 2, 
                    img_src: require('../assets/service/service2.jpg'), 
                },
                {
                    id: 3, 
                    img_src: require('../assets/service/service3.jpg'), 
                },
                {
                    id: 4, 
                    img_src: require('../assets/service/service4.jpg'), 
                },
                {
                    id: 5, 
                    img_src: require('../assets/service/service5.jpg'), 
                },
                {
                    id: 6, 
                    img_src: require('../assets/service/service6.jpg'), 
                },
            ],
        }),
        methods: {
            changeImage(i){
                console.log(i); 
                const url = this.imgStore.find(x => x.id === i).img_src;
                console.log(url);
                this.serviceImg = url; 
            }
        },
    }
</script>