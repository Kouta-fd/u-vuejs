<template>
  <div>
    <LikeHeader>
      <template v-slot:title>
        <h1>トータルのいいね数</h1>
      </template>
      <template v-slot:number>
        <h2>{{number}}</h2>
      </template>
    </LikeHeader>
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


