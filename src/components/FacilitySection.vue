<template>
    <section id="facility">
        <div class="container pt-5 pb-3">
            <div class="section-content mb-5 pt-3">
                <div class="row row-cols-1 row-cols-md-4 g-2">
                    <div class="col" v-for="(facility, i) in facilities" :key="i">
                        <div class="card p-3 pb-1 text-center mb-3 mx-auto" @mouseover="facility.hoverStatus = true" @mouseout="facility.hoverStatus = false" :id="facility.id" style="width: 90%;">
                            <img v-if="facility.hoverStatus" :src="facility.hoverImage" class="card-img-top img-fluid rounded-circle mx-auto mt-4" :alt="facility.title">
                            <img v-if="!facility.hoverStatus" :src="facility.image" class="card-img-top img-fluid rounded-circle mx-auto mt-4" :alt="facility.title">
                            <div class="card-body text-center pt-4 pb-3">
                                <h4 class="card-title mb-3">{{facility.title}}</h4>
                                <p class="card-text">{{facility.description}}</p> 
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
        name: 'FacilitySection',
        data: () => ({ 
            facilities: [
                {
                    id: '1',
                    title: 'মাতৃভাষায় বিজ্ঞানচর্চা',
                    description: 'বিজ্ঞান অভিধানে বিজ্ঞান সম্পর্কিত সকল শব্দের বিস্তারিত বিবরণ ও তথ্য-উপাত্ত সহজ-সাবলীলভাবে বাংলা ভাষায় উপস্থাপন করা হয়েছে।তাই বিজ্ঞান অভিধান এক্ষেত্রে তাদের গৃহশিক্ষকের মতো সহায়তা করবে।',
                    image: require('../assets/facilities/facility1.png'),
                    hoverImage: require('../assets/facilities/facility1-1.png'),  
                    hoverStatus: false
                },
                {
                    id: '2',
                    title: 'অনলাইন ও অফলাইন',
                    description: 'শিক্ষার্থীদের সুবিধার জন্য অফলাইন এবং অনলাইন দুভাবেই ব্যবহারের সুযোগ রয়েছে। যেকোনো শিক্ষার্থী সম্পূর্ণ বিনামূল্যেই গুগল প্লেস্টোর থেকে অ্যাপটি ইন্সটল করে ব্যবহার করতে পারবে।',
                    image: require('../assets/facilities/facility2.png'),
                    hoverImage: require('../assets/facilities/facility2-2.png'),
                    hoverStatus: false
                },
                {
                    id: '3',
                    title: 'অ্যাপ এবং ওয়েবসাইট',
                    description: 'বিজ্ঞান অভিধান অ্যাপ এবং ওয়েভভিত্তিক বিজ্ঞান শব্দকোষ যেখানে রয়েছে ১০ হাজারেরও বেশি বিজ্ঞান সংশ্লিষ্ট শব্দের বিস্তারিত বিবরণ।তাই শিক্ষার্থীরা যেকোন ডিভাইস থেকেই আমাদের কন্টেন্ট এবং এক্সেস করতে পারবে।',
                    image: require('../assets/facilities/facility3.png'),
                    hoverImage: require('../assets/facilities/facility3-3.png'),
                    hoverStatus: false
                },
                {
                    id: '4',
                    title: 'জীবনমূখী শিক্ষা',
                    description: 'সংজ্ঞা, সূত্র, সমার্থক শব্দ, প্রকারভেদ, উদাহরণ, নামকরণের ইতিহাস, গুরুত্বপূর্ণ বৈশিষ্ট্য, বাস্তবজীবনে ব্যবহারের মতো সেগমেন্টগুলো শিক্ষার্থীদের পূর্ণাঙ্গ জ্ঞান অর্জন এবং বিজ্ঞান বিষয়ে জানার আগ্রহকে বৃদ্ধি করবে।',
                    image: require('../assets/facilities/facility4.png'),
                    hoverImage: require('../assets/facilities/facility4-4.png'),
                    hoverStatus: false
                }
            ],
        }),
    }
</script>