<template>
    <div class="flex">
    
        <p class="digit mr-1 "> Butik Kapanış:  </p>
        <p class="digit mr-1 ">{{ $filters.two_digits(hours)   }} saat </p>
        <p class="digit mr-1"> {{  $filters.two_digits(minutes) + `:` + $filters.two_digits(seconds) }}</p>
  </div>
</template>

<script>


export default {
  name: 'countdown',
  components: {

  },
  props: {
    date: {
      type: String
    }
  },
  mounted () {
      console.log(this.date)
     window.setInterval(() => {
        this.now = Math.trunc((new Date()).getTime() / 1000);
    },1000);
  },
  computed: {
    dateInMilliseconds() {
      return Math.trunc(Date.parse(this.date) / 1000)
    },
    seconds() {
      return (this.dateInMilliseconds - this.now) % 60;
    },
    minutes() {
      return Math.trunc((this.dateInMilliseconds - this.now) / 60) % 60;
    },
    hours() {
      return Math.trunc((this.dateInMilliseconds - this.now) / 60 / 60) % 24;
    },
    days() {
      return Math.trunc((this.dateInMilliseconds - this.now) / 60 / 60 / 24);
    }
  },
  methods : {
 
  },
data () {
    return {
        now: Math.trunc((new Date()).getTime() / 1000),
     }
  },
}
</script>
<style >
 
</style>