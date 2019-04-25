<template>
  <div>
    <div class="container">
      <br>
      <div class="columns">
        <div class="column is-4">
          <p>Number of data :</p>
          <input class="input" type="number" v-on:keyup.enter="getmodulus()" v-model="dataLength">
          <small><i>*press enter to input</i></small>
        </div>
      </div>
      <table class="table" v-if="dataLengths.length !== 0">
        Result :
        <tr v-for="(data, index) in dataLengths" :key="index">
          <td>{{index+1}}</td>
          <td>{{data}}</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
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
            this.dataLengths.push('Hello')
            //  console.log(i + 'hello')  
          } else if (i % 5 == 0) {
            this.dataLengths.push('World')
            // console.log(i + 'world')
          } else {
            this.dataLengths.push('-')
            // console.log('-')
          }
        }
      }
    }
  }

</script>

