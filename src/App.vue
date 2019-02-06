<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <router-link to="/Kelas">Data Kelas </router-link>
    <router-link to="/siswa">Data Siswa</router-link>
    <router-view/> -->
  <h1>{{ nama }}</h1>
  <h2>Nama : <input v-model="nama" type="" name=""><br></h2>
  <h2>Nilai Anda : {{  nilai }}</h2>
  <button @click = "totalnilai">Click Me</button>
  <h2>1. Apakah Nama Ibukota Perancis ?</h2>
  <input type="radio" name="" v-model="soal1" value="Bandung">Bandung
  <input type="radio" name="" v-model="soal1" value="Paris">Paris
  <input type="radio" name="" v-model="soal1" value="Ciamis">Ciamis
  <input type="radio" name="" v-model="soal1" value="Berlin">Berlin<br>
  <h2>2. Berapakah  10  x 2 ?</h2>
  <input type="radio" name="" v-model="soal2" value="10">10
  <input type="radio" name="" v-model="soal2" value="15">15
  <input type="radio" name="" v-model="soal2" value="20">20
  <input type="radio" name="" v-model="soal2" value="5">5<br>
  <h2>3. Tanggal Berapakah HUT RI ?</h2>
  <input type="radio" name="" v-model="soal3" value="17">17 Agustus
  <input type="radio" name="" v-model="soal3" value="1">1 Agustus
  <input type="radio" name="" v-model="soal3" value="15">15 April
  <input type="radio" name="" v-model="soal3" value="31">31 Februari<br>
  </div>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'
*/

export default {
  name: 'App',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
    }
  },
  methods: {
    totalnilai(){
      if(this.soal1 == 'Paris' && this.soal2 == '20' && this.soal3 == '17') {
        this.nilai=+3
      }
      else if (this.soal1 == 'Paris' && this.soal2 == '20') {
        this.nilai=+2
      }
      else if (this.soal1 == 'Paris' && this.soal3 == '17') {
        this.nilai=+2
      }
      else if (this.soal2 == '20' && this.soal3 == '17') {
        this.niali=+2
      }
      else if (this.soal1 == 'Paris') {
        this.nilai=+1
      }
      else if (this.soal2 == '20') {
        this.nilai=+1
      }
      else if (this.soal3 == '17') {
        this.nilai=+1
      }
      else{
        this.nilai = 0
      }
    }
  }
  /*,
  components: {
    HelloWorld
  }*/
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
