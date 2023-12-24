<template>
    <div id="app">
        <PeakuWork class="work" v-for="(job, index) in jobs" :key="index" :job="job" />
    </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
import PeakuWork from './components/PeakuWork.vue';

export default {
    name: 'App',
    components: {
        //HelloWorld,
        PeakuWork
    },
    data() {
        return {
            jobs: [
                {
                    id: 1,
                    title: 'Frontend Developer',
                    requirements: ['HTML', 'CSS', 'JavaScript'],
                    company: 'Google',
                    location: 'Mountain View, CA',
                    salary: '2',
                    vacants: '1',
                    publicationDate: '2020-01-01',
                    img: 'https://kgo.googleusercontent.com/profile_vrt_raw_bytes_1587515358_10512.png'
                },
                {
                    id: 2,
                    title: 'Full Stack Developer',
                    requirements: ['HTML', 'CSS', 'JavaScript', 'Node.js', 'React'],
                    company: 'Microsoft',
                    location: 'Redmond, WA',
                    salary: '3',
                    vacants: '3',
                    publicationDate: '2020-01-02',
                    img: 'https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Microsoft_logo.svg/768px-Microsoft_logo.svg.png'
                },
                {
                    id: 3,
                    title: 'UX/UI Designer',
                    requirements: ['Sketch', 'Figma', 'Adobe XD'],
                    company: 'Apple',
                    location: 'Cupertino, CA',
                    salary: '3.5',
                    vacants: '2',
                    publicationDate: '2020-01-03',
                    img: 'https://upload.wikimedia.org/wikipedia/commons/f/fa/Apple_logo_black.svg'
                },
                {
                    id: 4,
                    title: 'Data Analyst',
                    requirements: ['SQL', 'Excel', 'Statistics'],
                    company: 'Amazon',
                    location: 'Seattle, WA',
                    salary: '2.5',
                    vacants: '4',
                    publicationDate: '2020-01-04',
                    img: 'https://i0.wp.com/arnimartinez.com/wp-content/uploads/2018/10/amazon.png?resize=225%2C225&ssl=1'
                },
                {
                    id: 5,
                    title: 'Mobile App Developer',
                    requirements: ['Swift', 'Kotlin', 'React Native'],
                    company: 'Facebook',
                    location: 'Menlo Park, CA',
                    salary: '3.8',
                    vacants: '2',
                    publicationDate: '2020-01-05',
                    img: 'https://img.freepik.com/vector-premium/vinnitsyaucrania24-enero-2021facebook-imagen-vectorial-icono-plano-letra-f-boton-color-azul-letra-aislada-sobre-fondo-blanco_736051-65.jpg'
                },
                {
                    id: 6,
                    title: 'Cybersecurity Analyst',
                    requirements: ['Cybersecurity', 'Firewalls', 'Encryption'],
                    company: 'Netflix',
                    location: 'Los Gatos, CA',
                    salary: '4.2',
                    vacants: '1',
                    publicationDate: '2020-01-06',
                    img: 'https://static.vecteezy.com/system/resources/previews/020/336/373/original/netflix-logo-netflix-icon-free-free-vector.jpg'
                },
                {
                    id: 7,
                    title: 'Cloud Solutions Architect',
                    requirements: ['AWS', 'Azure', 'Google Cloud'],
                    company: 'Tesla',
                    location: 'Palo Alto, CA',
                    salary: '4.5',
                    vacants: '2',
                    publicationDate: '2020-01-07',
                    img: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/bb/Tesla_T_symbol.svg/800px-Tesla_T_symbol.svg.png'
                },
                {
                    id: 8,
                    title: 'AI/Machine Learning Engineer',
                    requirements: ['Python', 'TensorFlow', 'PyTorch'],
                    company: 'SpaceX',
                    location: 'Hawthorne, CA',
                    salary: '5',
                    vacants: '1',
                    publicationDate: '2020-01-08',
                    img: 'https://cdn.icon-icons.com/icons2/2389/PNG/512/spacex_logo_icon_144865.png'
                },
                {
                    id: 9,
                    title: 'Blockchain Developer',
                    requirements: ['Blockchain', 'Smart Contracts', 'Solidity'],
                    company: 'Twitter',
                    location: 'San Francisco, CA',
                    salary: '3.7',
                    vacants: '3',
                    publicationDate: '2020-01-09',
                    img: 'https://img.freepik.com/vector-premium/nuevo-logotipo-twitter-x-2023-descarga-vector-logotipo-twitter-x_691560-10809.jpg'
                },
                {
                    id: 10,
                    title: 'DevOps Engineer',
                    requirements: ['Docker', 'Kubernetes', 'CI/CD'],
                    company: 'Uber',
                    location: 'San Francisco, CA',
                    salary: '4',
                    vacants: '2',
                    publicationDate: '2020-01-10',
                    img: 'https://static.vecteezy.com/system/resources/previews/027/127/501/original/uber-logo-uber-icon-transparent-free-png.png'
                },
                /* {
                    id: 11,
                    title: 'Product Manager',
                    requirements: ['Product Management', 'Agile', 'Market Analysis'],
                    company: 'LinkedIn',
                    location: 'Sunnyvale, CA',
                    salary: '4.2',
                    vacants: '1',
                    publicationDate: '2020-01-11',
                    img: 'https://example.com/linkedin.png'
                },
                {
                    id: 12,
                    title: 'Network Engineer',
                    requirements: ['Networking', 'Cisco', 'Security'],
                    company: 'Adobe',
                    location: 'San Jose, CA',
                    salary: '3.5',
                    vacants: '3',
                    publicationDate: '2020-01-12',
                    img: 'https://example.com/adobe.png'
                },
                {
                    id: 13,
                    title: 'Quality Assurance Tester',
                    requirements: ['Testing', 'Automation', 'Bug Tracking'],
                    company: 'Oracle',
                    location: 'Redwood City, CA',
                    salary: '3',
                    vacants: '2',
                    publicationDate: '2020-01-13',
                    img: 'https://example.com/oracle.png'
                },
                {
                    id: 14,
                    title: 'IT Support Specialist',
                    requirements: ['IT Support', 'Troubleshooting', 'Customer Service'],
                    company: 'PayPal',
                    location: 'San Jose, CA',
                    salary: '2.5',
                    vacants: '4',
                    publicationDate: '2020-01-14',
                    img: 'https://example.com/paypal.png'
                },
                {
                    id: 15,
                    title: 'Content Marketing Manager',
                    requirements: ['Content Marketing', 'SEO', 'Social Media'],
                    company: 'Airbnb',
                    location: 'San Francisco, CA',
                    salary: '4.2',
                    vacants: '2',
                    publicationDate: '2020-01-15',
                    img: 'https://example.com/airbnb.png'
                },
                {
                    id: 16,
                    title: 'Technical Writer',
                    requirements: ['Technical Writing', 'Documentation', 'Communication'],
                    company: 'Square',
                    location: 'San Francisco, CA',
                    salary: '3.7',
                    vacants: '1',
                    publicationDate: '2020-01-16',
                    img: 'https://example.com/square.png'
                },
                {
                    id: 17,
                    title: 'Human Resources Manager',
                    requirements: ['HR Management', 'Recruitment', 'Employee Relations'],
                    company: 'Salesforce',
                    location: 'San Francisco, CA',
                    salary: '4.5',
                    vacants: '2',
                    publicationDate: '2020-01-17',
                    img: 'https://example.com/salesforce.png'
                },
                {
                    id: 18,
                    title: 'Graphic Designer',
                    requirements: ['Graphic Design', 'Adobe Creative Suite', 'Creativity'],
                    company: 'VMware',
                    location: 'Palo Alto, CA',
                    salary: '3.8',
                    vacants: '1',
                    publicationDate: '2020-01-18',
                    img: 'https://example.com/vmware.png'
                },
                {
                    id: 19,
                    title: 'Customer Success Manager',
                    requirements: ['Customer Success', 'Client Relationship', 'Communication'],
                    company: 'IBM',
                    location: 'Armonk, NY',
                    salary: '4',
                    vacants: '3',
                    publicationDate: '2020-01-19',
                    img: 'https://example.com/ibm.png'
                },
                {
                    id: 20,
                    title: 'Legal Counsel',
                    requirements: ['Legal', 'Contracts', 'Law Degree'],
                    company: 'Intel',
                    location: 'Santa Clara, CA',
                    salary: '5',
                    vacants: '1',
                    publicationDate: '2020-01-20',
                    img: 'https://example.com/intel.png'
                } */
            ]
        }
    }
}
</script>

<style>
#app {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}

.work:hover{
    box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.1);
}
</style>
