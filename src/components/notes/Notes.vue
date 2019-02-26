<template>
  <div class="notes columns">

    <table class="table box column">
      <thead>
        <tr>
          <th>Student</th>
          <th>Rank</th>
          <th>Average</th>
          <th>Evolution</th>
          <th>ID</th>
        </tr>
      </thead>
      <tfoot>
        <tr>
          <th>Student</th>
          <th>Rank</th>
          <th>Average</th>
          <th>Evolution</th>
          <th>ID</th>
        </tr>
      </tfoot>
      <tbody>
        <tr v-for="student in students" :key="student.rank" @click="studentInfos(student)">
          <th> {{ student.name }} </th>
          <td> {{ student.rank }} </td>
          <td> {{ student.average }} </td>
          <td> {{ student.evolution }} </td>
          <td> {{ student.id }} </td>
        </tr>
      </tbody>
    </table>
    <Student v-if="currentStudent" :student="currentStudent" id="stats" class="column box"/>

  </div>
</template>

<script>
import Student from "./Student.vue"

export default {
  name: 'Notes',
  components:{
    Student
  },
  props: {
  },
  data: function (){
      return{
        view: 0,
        currentStudent: null,
        students: [
          {
            name: "Olivier BENABEN",
            id: "21602597",
            rank: 1,
            average: 19.75,
            evolution: "⸳"
          },
          {
            name: "Hugo HENROTTE",
            id: "321",
            rank: 2,
            average: 19.75,
            evolution: '▴',
          },
          {
            name: "Guillaume MONTFORT",
            id: "123",
            rank: 3,
            average: 19.75,
            evolution: '▾',
          }
        ]
      }
    },
  methods:{
    studentInfos: function(student){
      this.$data.view = 1;
      this.$data.currentStudent = student;
    }
  }
}
</script>

<style scoped>
.notes{
  width: 100vw;
  justify-content: center;

  padding: 15px;
  padding-top: 10vh;
}

table{
  max-width: 590px;
  padding-left: 5vw;

  max-height: 80vh;
  overflow: auto;
}

#stats{
  margin-left: 20px;
}

*{
  text-align: center;
}
</style>
