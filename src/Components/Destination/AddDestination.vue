<template>
  <div class="container p-4 bg-white border mb-4">
    <h5>Create new Destination:</h5>
    <form @submit.prevent="addDestination" class="row">
      <div class="col-12 col-md-6 p-1">
        <input
          type="text"
          class="form-control"
          v-model="newDestination.name"
          placeholder="Destination Name..."
          required
        />
      </div>
      <div class="col-12 col-md-6 p-1">
        <input
          type="text"
          class="form-control"
          v-model="newDestination.days"
          placeholder="Destination Days..."
          required
        />
      </div>
      <div class="col-12 col-md-6 p-1">
        <input
          type="number"
          class="form-control"
          v-model.number="newDestination.price"
          placeholder="Destination Cost..."
          required
        />
      </div>
      <button type="submit" class="btn btn-success col-12 col-md-6 p-1">
        Add Destination
      </button>
    </form>
  </div>
</template>
<script setup>
import { reactive } from "vue";
const newDestination = reactive({
  name: "",
  days: "",
  price: "",
  funFact: "",
});

function addDestination() {
  console.log(newDestination);
}
</script>