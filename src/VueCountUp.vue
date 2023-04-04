<template>
    <span ref="countup"></span>
</template>

<script>
import { CountUp } from 'countup.js'
export default {
    name: 'VueCountUp',
    data() {
        return {
            numAnim: null
        }
    },
    mounted() {
        this.initCountUp()
    },
    computed: {
        options() {
            return {
                startVal: this.start,
                decimal: this.decimal,
                duration: this.duration
            }
        }
    },
    methods: {
        initCountUp() {
            this.numAnim = new CountUp(this.$refs.countup,
                this.end,
                this.options)
            this.numAnim.start()
        }
    },
    props: {
        start: {
            type: Number,
            default: 0
        },
        end: {
            type: Number,
            default: 2017
        },
        decimal: {
            type: Number,
            default: 0
        },
        duration: {
            type: Number,
            default: 2.5
        },
        options: {
            type: Object
        }
    }
}
</script>