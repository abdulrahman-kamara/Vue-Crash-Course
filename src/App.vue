<template>
<div class="container">
  <Header title="Task Tracker"/>
  <Tasks :tasks="tasks"/>
</div>

</template>

<script>
import Header from './components/Header'
import Tasks from './components/Tasks'

export default {
  name: 'App',
  components: {
    Header,
    Tasks
  },
  data() {
    return {
      tasks: []
    }
  },
  create() {
    this.tasks = [
      {
        id: 1,
        text: 'Meeting with myself',
        day: 'Octobre 14 at 14h',
        remindeer: true,
      },
      {
        id: 2,
        text: 'Meeting with myfriend',
        day: 'Octobre 16 at 14h',
        remindeer: true,
      },
      {
        id: 3,
        text: 'Start to work',
        day: 'Octobre 18 at 09h',
        remindeer: false,
      }
    ]
  
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
    font-family: Arial, Helvetica, sans-serif;
}

.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  max-height :300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius:5px;
}
.btn {
  display: inline-block;
  background: black;
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 5px;
border: radius 5px;
cursor: pointer;
text-decoration: none;
font-size: 15px;
font-family: inherit;
}
</style>
