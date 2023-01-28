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
            <div id="app">
              <div>
                {{ uName }}
              </div>
              <div>
                {{ uAge }}
              </div>
              <div>
                {{ myMeal.theMeal }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
// using ref function for string, int
// using reactive function for object
import { ref, reactive } from "vue";

const uName = ref("Amir");
const uAge = ref(25);
const myMeal = reactive({
  theMeal: "Pizza",
});

setTimeout(function () {
  uName.value = "Hassan";
  uAge.value = 99;
  myMeal.theMeal = "Burger";
}, 2000);

// use composition API with basic syntax script
// import { ref, reactive } from "vue";

// export default {
//   setup() {
//     const uName = ref("Amir");
//     const uAge = ref(25);
//     const myMeal = reactive({
//       theMeal: "Pizza",
//     });

//     setTimeout(function () {
//       uName.value = "Hassan";
//       uAge.value = 99;
//       myMeal.theMeal = "Burger";
//     }, 2000);

//     return { testReturn: myMeal };
//   },
// };
</script>
