<template>
  <div>
    <section class="container padding">
      <h6>What we offer</h6>
      <h3 class="column-6" style="margin-bottom: 2rem">
        Some highlights of our favorite projects we've done for forward thinking
        clients.
      </h3>
      <br />
      <div class="service-img">
        <img
          src="@/assets/img/idea/atlantic-factorial.png"
          alt="atlantic-factorial"
        />
      </div>
    </section>
    <section class="container padding">
      <div class="flex flex-jc-sb flex-wrap">
        <AppServiceCard
          v-for="(card, i) in cardList"
          :key="i"
          :card-obj="card"
          class="column-6 card"
        />
      </div>
    </section>
  </div>
</template>
<script>
import AppServiceCard from '@/components/service/AppServiceCard'
export default {
  components: {
    AppServiceCard,
  },
  data() {
    return {
      cardList: [
        {
          title: 'Web development',
          description:
            'Tap into our deep web development expertise to build any web solution that your company needs, from  dynamic websites to complex enterprise-sized web solutions.',
          badgeList: ['Frontend Development', 'Backend Development'],
        },
        {
          title: 'Mobile Development',
          description:
            'Steering clients  through digital transformation, we build intuitive and engaging  Android, iOS, and cross-platform for businesses that your end users can adapt to quickly.',
          badgeList: ['Hybrid Apps', 'Native Apps'],
        },
        {
          title: 'Incubation and Acceleration',
          description:
            'With exclusive access to resources, tools, and services, we support your startup business and help you grow your network of mentors, investors and founders.',
          badgeList: ['Incubation', 'Acceleration'],
        },
        {
          title: 'Software Testing/Quality Assurance',
          description:
            'With our unparalleled technical expertise, we implement quality testing frameworks and automation expertise using current testing trends.',
          badgeList: [
            'Automated Tests',
            'Manual Test',
            'Performance Test',
            'Security Test',
          ],
        },
        {
          title: 'Application Maintenance and Support',
          description:
            'Keeping your application online, secure, updated and bug-free is our main goal, while we deal and resolve real time problems your  application might encounter on a day-to-day operational level.',
          badgeList: ['Maintenance', 'Upgrade', 'Support'],
        },
        {
          title: 'Research and Development',
          description:
            'We perform original investigations and research findings to strengthen your software engineering, technical implementation or research thesis, which can be used to create improved technologies. We have talents, labs, processes and infrastructures to deliver world class results to you.',
          badgeList: ['Research labs', 'Research Findings', 'Reporting'],
        },
        {
          title: 'Cloud and Enterprise Application Development',
          description:
            'We develop bespoke and streamlined enterprise solutions to automate your internal processes, drive business efficiency and flexibility, and provide advanced insights into your business operations and employees.',
          badgeList: [
            'ERP',
            'CRM',
            'HR',
            'Accounting',
            'Supply Chain',
            'Logistics',
          ],
        },
        {
          title: 'Devops as a service',
          description:
            'We offer cloud and devops solutions aimed at high performance, scalability, and agility at a reduced cost to maximize ROI, software availability,  cloud security, and continuous integrations allowing you to  run your solutions as fast as you run your business.',
          badgeList: ['Devops', 'Cloudops'],
        },
        {
          title: 'UI/UX and Product Design',
          description:
            'We are a design first development company. Projects are driven by designers and they make sure design and experiences translate to code. With expressive design, we give life to brands and create a synergy between the brand and the user.',
          badgeList: ['UI/UX', 'Product Design', 'Branding'],
        },
        {
          title: ' Emergency and Response',
          description:
            'This is a key service offered to businesses in need of quick  response to their business or application needs. Our dedicated emergency and response team are always available on a 24/7 hour basis to streamline your processes and give life to dying businesses or solutions.',
          badgeList: ['Support', 'Development', 'Management'],
        },
        {
          title: 'Data Analytics/AI/ML',
          description:
            'With our decades of expertise in the areas of Artificial intelligence, deep learning, machine learning, and data analysis; we build highly intelligent, automated, and analytical solutions for businesses to fast-track your problem-solving capabilities.',
          badgeList: ['AI', 'ML', 'Data Analytics', 'Bots', 'Chatbots'],
        },
        {
          title: 'Software Programming Mentorship and Consulting',
          description:
            'Business goals, technical requirements, project scoping and programing mentorship as we push the edge of innovations with our technical competencies and our delivery track record.',
          badgeList: ['Internship', 'Training', 'Consultation'],
        },
      ],
    }
  },
}
</script>
<style lang="scss" scoped>
.service-img {
  width: 100%;
  height: 15rem;
  @include breakpoint-up(large) {
    height: 30.1875rem;
  }
  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
</style>
