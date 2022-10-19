<template>
  <div id="app">
    <h3>Example</h3>
    <hr />
    <form @submit.prevent="addSubject" class="inputForm">
      <label for="">Enter new subject: </label>
      <input v-model="newSubject" type="text" />
      <button>Add subject</button>
    </form>
    <hr />
    <ul>
      <li v-for="(subject, index) in allSubjects">
        {{ subject.content }}
        <button @click="removeSubject(index)">Delete</button>
      </li>
    </ul>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const newSubject = ref('Mittwoch');
    const allSubjects = ref([]);

    function addSubject() {
      allSubjects.value.push({
        content: newSubject.value,
      });
      newSubject.value = '';
      console.log(allSubjects.value);
    }

    function removeSubject(index) {
      console.log('remove' + index);
      allSubjects.value.splice(index, 1);
    }

    return {
      newSubject,
      addSubject,
      allSubjects,
      removeSubject,
    };
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}

h3 {
  margin-bottom: 20px;
}

.inputForm {
  display: flex;
  justify-content: space-between;
}

ul li button {
  margin-left: 35px;
}
</style>