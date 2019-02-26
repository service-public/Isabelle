<template>
  <div class="calendar">
    <table class="table box">
      <thead>
        <tr>
          <th> </th>
          <th>9h</th>
          <th></th>
          <th>11h</th>
          <th></th>
          <th>13h</th>
          <th></th>
          <th>14h</th>
          <th></th>
          <th>16h</th>
          <th></th>
          <th>18h</th>
        </tr>
      </thead>
      <tfoot>
        <tr>
          <th> </th>
          <th>9h</th>
          <th></th>
          <th>11h</th>
          <th></th>
          <th>13h</th>
          <th></th>
          <th>14h</th>
          <th></th>
          <th>16h</th>
          <th></th>
          <th>18h</th>
        </tr>
      </tfoot>
      <tbody>
        <tr>
          <th>L</th>
          <td></td>
          <td class=""> {{ week[0][0] }} </td>
          <td></td>
          <td class="button is-primary"> {{ week[0][1] }} </td>
          <td></td>
          <td> {{ week[0][2] }} </td>
          <td></td>
          <td class="button is-danger"> {{ week[0][3] }} </td>
          <td></td>
          <td class="button is-danger"> {{ week[0][4] }} </td>
          <td></td>
        </tr>
        <tr>
          <th>M</th>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-primary">Quantique</td>
          <td></td>
          <td></td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
        </tr>
        <tr>
          <th>M</th>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-primary">Quantique</td>
          <td></td>
          <td></td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
        </tr>
        <tr>
          <th>J</th>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-primary">Quantique</td>
          <td></td>
          <td></td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
        </tr>
        <tr>
          <th>V</th>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-primary">Quantique</td>
          <td></td>
          <td></td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
          <td class="button is-danger">Maths</td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>

export default {
  name: 'calendar',
  components:{
  },
  props: {
  },
  data: function (){
      return{
        week: [
          ['', 'Méca', '', 'Méca', 'Anglais'],
          ['', '', '', 'Info', 'Info'],
          ['Quantique', 'Electromag', '', 'Quntique', 'Electromag'],
          ['Proba', 'Proba', '', '', ''],
          ['Info', 'Proba', '', 'Info', ''],
        ]
      }
    },
  methods:{
  }
}
</script>

<style scoped>
.calendar{
  width: 100vw;
  justify-content: center;
  padding-top: 10vh;
}

table{
  max-width: 770px;
  padding-left: 5vw;
}

*{
  text-align: center;
}
</style>
