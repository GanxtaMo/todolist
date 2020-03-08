<template>
  <div>
    <h1>To do list</h1>
    <div class="container">
      <input v-model="input" type="text" />
      <b-btn @click="addInput()" variant="success">Add </b-btn>
    </div>
    <div class="container">
      <b-list-group id="li">
        <b-list-group-item id="liC"
          v-for="l in list"
          :key="l.index"
          :class="{ striker: l.done }"
          @click="strikeThrough(l)"
        >
          {{ l.title }}</b-list-group-item
        >
      </b-list-group>
    </div>
  </div>
</template>

<script>
export default {
  name: "to_do",
  data() {
    return {
      list: [],
      input: null
    };
  },

  methods: {
    addInput() {
      this.list.push({
        id: this.index,
        title: this.input,
        done: false
      });
    },
    strikeThrough(l) {
      l.done = !l.done;
      alert("Great job :)")
    }
  }
};
</script>


<style scoped>
h1{
    text-decoration: underline;
}
#li{
    margin-top: 10%;
    margin-left: 20%;
    width: 60%;
}
#liC{
    margin-bottom: 10%;
    border: 0px transparent;
}
.striker {
  text-decoration: line-through;
  background-color: rgb(47, 155, 79);
  pointer-events: none;
  
}
</style>
