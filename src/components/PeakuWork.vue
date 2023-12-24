<template>
    <div class="card mb-3 w-75">
        <div class="row g-0 p-3">
            <div class="col text-start img me-3">
                <img :src="job.img"
                    class="img-fluid rounded-start" alt="...">
            </div>
            <div class="col">
                <div class="card-body p-0 h-100 position-relative">
                    <div class="top d-flex position-absolute top-0 start-0">
                        <h5 class="text-start fw-bold me-3 m-0">{{ job.title }}</h5>
                        <div class="me-2" v-for="(requirement, index) in job.requirements" :key="index">
                            <p class="m-0">{{ requirement }}</p>
                        </div>
                    </div>
                    <div class="bottom d-flex position-absolute bottom-0 start-0 w-100">
                        <div class="item d-flex">
                            <img :src="require('@/assets/building.svg')">
                            <p class="m-0">{{ job.company }}</p>
                        </div>
                        <div class="item d-flex">
                            <img :src="require('@/assets/marker.svg')">
                            <p class="m-0">{{ job.location }}</p>
                        </div>
                        <div class="item d-flex">
                            <img :src="require('@/assets/coins.svg')">
                            <p class="m-0">$ {{ job.salary }}M COP</p>
                        </div>
                        <div class="item d-flex">
                            <img :src="require('@/assets/users.svg')">
                            <p class="m-0">{{ job.vacants }} Vacantes</p>
                        </div>
                        <div class="item d-flex">
                            <img :src="require('@/assets/calendar-clock.svg')">
                            <p class="m-0">{{ job.publicationDate }} </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PeakuWork',
    props: {
        job: Object
    },
    data() {
        return {
            

        }
    },
    methods: {

    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
    width: 70px;
    height: 70px;
}

.img {
    max-width: 70px;
}

.top p {
    font-size: 14px;
    padding: 1px 6px 1px 6px;

}

.top div {

    border: 1px solid gray;
    border-radius: 25px;
    text-align: center;

}

.bottom {
    flex-basis: 0;
    flex-grow: 1;
}

.bottom p {
    font-size: 14px;
    padding: 1px 6px 1px 6px;

}

.item {
    flex-grow: 1;
}

.item img {
    width: 20px;
    height: 20px;
}</style>