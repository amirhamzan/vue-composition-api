<template>
  <link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css"
  />
  <div class="container mt-5 text-center">
    <div class="row mx-auto">
      <div class="col">
        <div class="card">
          <div class="card-body">
            <div id="app">{{ uName }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
import { ref } from "vue";

const uName = ref("Amir");

setTimeout(function () {
  uName.value = "Hassan";
}, 2000);
</script>