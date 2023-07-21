<script setup >
let msg = "Hallo Andika Ganteng";
let blue = "#00f"
let rawHtml = `<span style="color : blue" >Ini Memang Biru</span>`
let headName = "<h1>Nama saya muhamaddika</h1>"
</script>

<template>
  <div>
    <span>{{ msg }}</span> <br>
    <span style="color: blue"></span>
    <span v-html="rawHtml"></span>
    <span v-html="headName"></span> 
    <button v-bind:aria-disabled="isButtonDisabled">Tombol</button>
  </div> <br>
  {{ text }}
  <br><br>
  <button v-on:click="reversetxt()">balikeun</button>
</template>

<script>
export default {
  data() {
    return {
      text: 'Hallo Dunia'
    }
  },
  methods: {
    reversetxt(){
      this.text = this.text.split('').reverse().join('')
    }
  }
}
</script>