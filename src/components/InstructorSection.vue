<template>
    <section id="instructor">
        <div class="container">
            <div class="section-title-div text-center my-5">
                <h3 class="section-title mb-0">ইন্সট্রাক্টর</h3>
            </div>
            <div class="section-content mb-5">
                <div class="row row-cols-1 row-cols-md-4 g-2">
                    <div class="col" v-for="(instructor, i) in instructors" :key="i">
                        <div class="card p-3 pb-1 text-center bg-white mb-3 mx-auto" :id="instructor.id" style="width: 80%;">
                            <img :src="instructor.image" class="card-img-top img-fluid rounded-circle mx-auto" :alt="instructor.name" style="width: 60%">
                            <div class="card-body text-center pt-4 pb-3">
                                <h4 class="card-title mb-3">{{instructor.name}}</h4>
                                <small class="card-text">{{instructor.institution}}</small> 
                                <p class="card-icon mt-3">
                                    <a :href="instructor.mail">
                                        <span class="material-icons-outlined">g_mobiledata</span>
                                    </a>
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
    import '../css/style.css'; 
    export default {
        name: "InstructorSection",
        data: () => ({
            instructors: [
                {
                    id: '1',
                    name: 'গোলাম রব্বানী',
                    institution: 'সিলেট কৃষি বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor1.jpg')
                },
                {
                    id: '2',
                    name: 'মারজান হক',
                    institution: 'বাংলাদেশ কৃষি বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor2.jpg')
                },
                {
                    id: '3',
                    name: 'মোহাম্মাদ আলী',
                    institution: 'ঢাকা বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor3.jpg')
                },
                                {
                    id: '4',
                    name: 'ইরফানুল হক',
                    institution: 'বঙ্গবন্ধু শেখ মুজিবুর রহমান বিজ্ঞান ও প্রযুক্তি বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor4.jpg')
                },
                {
                    id: '5',
                    name: 'নাইম মির',
                    institution: 'জাতীয় বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor5.jpg')
                },
                {
                    id: '6',
                    name: 'তানহা তাবাসসুম',
                    institution: 'শাহজালাল বিজ্ঞান ও প্রযুক্তি বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor6.jpg')
                },
                {
                    id: '7',
                    name: 'কৃষনেন্দু সাহা',
                    institution: 'হাজী দানেশ বিজ্ঞান ও প্রযুক্তি বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor7.jpg')
                },
                {
                    id: '8',
                    name: 'অভিজিৎ দত্ত',
                    institution: 'যশোর বিজ্ঞান ও প্রযুক্তি বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor8.jpg')
                },
                {
                    id: '9',
                    name: 'আশরাফ সিদ্দিকী',
                    institution: 'ঢাকা মেডিকেল কলেজ',
                    mail: '#',
                    image: require('../assets/instructors/instructor9.jpg')
                },
                {
                    id: '10',
                    name: 'নুরুল আলম',
                    institution: 'নানজিন টেক ইউইভার্সিটি',
                    mail: '#',
                    image: require('../assets/instructors/instructor10.jpg')
                },
                {
                    id: '11',
                    name: 'হাবিবুর রহমান',
                    institution: 'যশোর বিজ্ঞান ও প্রযুক্তি বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor11.jpg')
                },
                {
                    id: '12',
                    name: 'তরিকুল ইসলাম',
                    institution: 'জাতীয় বিশ্ববিদ্যালয়',
                    mail: '#',
                    image: require('../assets/instructors/instructor12.jpg')
                },
            ],
        }),
    }
</script>