<template>
  <div>
    <input type="number" v-on:keyup.enter="getmodulus()" v-model="dataLength">
    <ul>
      <li v-for="(data, index) in dataLengths" :key="index">{{data}}</li>
    </ul>
  </div>
</template>

<script>
  // for (i = 1; i <= this.dataLength; i++) {
  //   if (i % 3 == 0) {
  //      console.log(i + 'hello')
  //   } else if (i % 5 == 0) {
  //      console.log(i + 'world')
  //   }
  //   console.log(i)
  // }




  export default {
    mounted() {
      console.log((1, 3));
    },

    data() {
      return {
        dataLengths: []
      }
    },
    methods: {
      getmodulus() {
        var i = 1;
        var num = this.dataLength;
        this.dataLengths = [];
        for (i = 1; i <= num; i++) {          
          if (i % 3 == 0) {
            this.dataLengths.push(i + ' hello')
          //  console.log(i + ' hello')  
          } else if (i % 5 == 0) {
             this.dataLengths.push(i + 'world')
            // console.log(i + ' world')
          } else {
            this.dataLengths.push(i)
            // console.log(i)
          }
        }
        
      }
    }
  }

</script>


<style>

</style>
