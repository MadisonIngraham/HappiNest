<template>
  <div class="dropdown">
    <button
      class="btn btn-secondary dropdown-toggle"
      type="button"
      id="dropdownMenuButton"
      data-toggle="dropdown"
      aria-haspopup="true"
      aria-expanded="false"
    >Log A Chore</button>
    <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
      <p class="dropdown-item" @click.prevent="addDishes">Washed Dishes +3</p>
      <p class="dropdown-item" @click.prevent="addVacuum">Vacuumed +2</p>
      <p class="dropdown-item" @click.prevent="addCounters">Wiped Down Counters +1</p>
      <p class="dropdown-item" @click.prevent="addDust">Dusted +1</p>
      <p class="dropdown-item" @click.prevent="addLawn">Mowed Lawn +3</p>
      <p class="dropdown-item" @click.prevent="addWeeds">Pulled Weeds +4</p>
      <p class="dropdown-item" @click.prevent="addTrash">Took Out Trash +2</p>
      <p class="dropdown-item" @click.prevent="addFridge">Cleaned Fridge +2</p>
      <p class="dropdown-item" @click.prevent="addSwept">Swept +2</p>
      <p class="dropdown-item" @click.prevent="addMop">Mopped +3</p>
      <p class="dropdown-item" @click.prevent="addBathroom">Cleaned Bathroom +5</p>
    </div>
  </div>
</template>

<script>
import Room from "./Room";
export default {
  name: "dropdown",
  props: ["dropData"],
  methods: {
    addDishes() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addDishes", ids);
    },
    addVacuum() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addVacuum", ids);
    },
    addCounters() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addCounters", ids);
    },
    addDust() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addDust", ids);
    },
    addLawn() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addLawn", ids);
    },
    addWeeds() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addWeeds", ids);
    },
    addTrash() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addTrash", ids);
    },
    addFridge() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addFridge", ids);
    },
    addSwept() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addSwept", ids);
    },
    addMop() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addMop", ids);
    },
    addBathroom() {
      let ids = {
        houseId: this.$route.params.id,
        profileId: this.dropData._id
      };
      this.$store.dispatch("addBathroom", ids);
    }
  }
};
</script>

<style scoped>
template {
  --blue: #375a7f;
  --indigo: #6610f2;
  --purple: #6f42c1;
  --pink: #e83e8c;
  --red: #e74c3c;
  --orange: #fd7e14;
  --yellow: #f39c12;
  --green: #00bc8c;
  --teal: #20c997;
  --cyan: #3498db;
  --white: #fff;
  --gray: #999;
  --gray-dark: #303030;
  --primary: #375a7f;
  --secondary: #444;
  --success: #00bc8c;
  --info: #3498db;
  --warning: #f39c12;
  --danger: #e74c3c;
  --light: #999;
  --dark: #303030;
}
button {
  color: black;
  background-color: var(--warning);
  border-color: black;
}
#dropdownMenuButton {
  width: 98%;
  border-radius: 0;
}
</style>
