<template>
    <div class="tags has-addons is-marginless">
        <span class="tag is-marginless link is-dark is-medium" @click="scrollTop()"><icon name="arrow-up"/></span>
        <span class="tag is-marginless link is-dark is-medium" @click="scrollBottom()"><icon name="arrow-down"/></span>
    </div>
</template>

<script>
const animateScrollTo = require('./animated-scroll-to')

export default {
    methods: {
        scrollTop() {
            this.scrollTO(0)
        },
        scrollBottom() {
            this.scrollTO(document.body.scrollHeight)
        },
        scrollTO(offset) {
            animateScrollTo(offset, {
                speed: 500,
                minDuration: 250,
                maxDuration: 1000
            })
        }
    }
}
</script>
