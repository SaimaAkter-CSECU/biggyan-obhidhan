<template>
    <section id="member">
        <div class="container">
            <div class="section-title-div text-center my-5">
                <h3 class="section-title mb-0">টিম মেম্বার</h3>
            </div>
            <div class="section-content mb-5">
                <div class="row row-cols-1 row-cols-md-4 g-2">
                    <div class="col" v-for="(member, i) in members" :key="i">
                        <div class="card p-3 pb-2 text-center bg-white mb-3 mx-auto" :id="member.id" style="width: 80%;">
                            <img :src="member.image" class="card-img-top img-fluid rounded-circle mx-auto" :alt="member.name" style="width: 60%">
                            <div class="card-body text-center pt-4 pb-3">
                                <h4 class="card-title mb-3">{{member.name}}</h4>
                                <small class="card-text">{{member.designation}}</small> 
                                <p class="card-icon mt-3">
                                    <a :href="member.mail">
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

    export default{
        name: 'TeamMemberSection',
                data: () => ({
                members: [
                    {
                        id: '1',
                        name: 'আবদুল্লাহ আল মামুন',
                        designation: 'ফাউন্ডার',
                        mail: '#',
                        image: require('../assets/members/member1.jpg')
                    },
                    {
                        id: '2',
                        name: 'শামস আল শাফিন',
                        designation: 'প্রজেক্ট ম্যানেজার',
                        mail: '#',
                        image: require('../assets/members/member2.jpg')
                    },
                    {
                        id: '3',
                        name: 'সাব্বির হোসাইন',
                        designation: 'টিম লিডার',
                        mail: '#',
                        image: require('../assets/members/member3.jpg')
                    },
                    {
                        id: '4',
                        name: 'ইয়াছির আরাফাত',
                        designation: 'ডেভেলপার',
                        mail: '#',
                        image: require('../assets/members/member4.jpg')
                    },
                    {
                        id: '5',
                        name: 'শোভন মাহমুদ',
                        designation: 'ডিজাইনার & ডেভেলপার',
                        mail: '#',
                        image: require('../assets/members/member5.jpg')
                    },
                    {
                        id: '6',
                        name: 'আবদুল্লাহ জাওয়াদ খান',
                        designation: 'ডেভেলপার',
                        mail: '#',
                        image: require('../assets/members/member6.jpg')
                    },
                    {
                        id: '7',
                        name: 'ফয়জুর রহমান',
                        designation: 'মার্কেটিং ম্যানাজার',
                        mail: '#',
                        image: require('../assets/members/member7.jpg')
                    }
                ],
            }),
    }
</script>
