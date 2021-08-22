<template>
  <div>
    <LikeHeader></LikeHeader>
    <h2>{{number}}</h2>
    <LikeNumber :total-number="number" @my-click="incrementNumber"></LikeNumber>
    <LikeNumber :total-number="number"></LikeNumber>
  </div>
</template>

<script>
  import LikeNumber from './components/LikeNumber'
  import LikeHeader from './components/LikeHeader'
  export default {
    data() {
      return {
        number: 10
      }
    },
    components: {
      LikeNumber,
      LikeHeader
    },
    methods: {
      incrementNumber(value) {
        this.number = value
      }
    }
  };
</script>


