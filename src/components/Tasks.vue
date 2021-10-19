<template>
    <div :key="task.id" v-for="task in tasks">

        <h3>{{ tasks.text }}</h3>

    </div>
</template>

<script>
import Tasks from './Tasks'

export default {

name: "Tasks",
props: {
    tasks: Array,
},
components:{
    Tasks,
}
}


</script>