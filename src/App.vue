<template>
  <div id="app">
    <div class="container">
      <div class="row header">
        <div class="col-lg-12">
          <h2>What I do Today ?</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <div class="row">
              <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas col-lg-12 text-start mt-2">
                <div class="form-check">
                  <ItemTugas v-bind:tugasSaya="tugasSaya" />
              </div>
            </div>
          </div>
          </div>
        </div>  
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";

import ItemTugas from "./components/ItemTugas.vue";

export default {
  name: "app",
  data: function() {
    return {
    tugas: [
      {
        id: 1,
        namaTugas: "Membersihkan Toilet",
        isDone: false
      },
      {
        id: 2,
        namaTugas: "Makan Bakso",
        isDone: false
      },
      {
        id: 3,
        namaTugas: "Gym Fit",
        isDone: false
      },
      {
        id: 4,
        namaTugas: "Istirahat 8 Jam",
        isDone: false
      },
    ]
    };
  },
  components: {
    ItemTugas
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.header{
  background: #1abc9c;
}
.header h2 {
  margin: 20px;
}

.tugas{ 
  margin-bottom: 30px;
}

.tugas .item{
  font-size: 20px;
}

.item-completed {
  color:#1abc9c;
}
</style>
