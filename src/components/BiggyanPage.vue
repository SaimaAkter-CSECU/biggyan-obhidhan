<template>
    <div>
        <HeaderSection />
        <BannerSection />
        <ServiceSection />
        <AboutSection />
        <FacilitySection />
        <TeamMemberSection />
        <InstructorSection />
        <FooterSection />
    </div>
</template>

<script>
  import HeaderSection from './HeaderSection.vue'
  import BannerSection from './BannerSection.vue'
  import ServiceSection from './ServiceSection';
  import AboutSection from './AboutSection.vue'
  import FacilitySection from './FacilitySection.vue'
  import TeamMemberSection from './TeamMemberSection.vue'
  import InstructorSection from './InstructorSection.vue'
  import FooterSection from './FooterSection.vue'

  export default {
    name: 'BiggyanPage',
    components: {
      HeaderSection, 
      BannerSection, 
      ServiceSection, 
      AboutSection,
      FacilitySection,
      TeamMemberSection,
      InstructorSection, 
      FooterSection
    }
  }
</script>