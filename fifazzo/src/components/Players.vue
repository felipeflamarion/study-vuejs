<template>
  <div id="players">
    <h1>Players</h1>

    <div class="match">

      <div class="home">
        <div class="header">
          <span>{{ home.name }}</span>
          <img src="~@/assets/logo-psg.png" />
        </div>

        <div class="squad">
          <div v-for="player in home.squad" :key="player.num">
            {{ player.name }}
          </div>
        </div>
      </div>

      <div class="away">
        <div class="header">
          <span>{{ away.name }}</span>
          <img src="~@/assets/logo-real.png" />
        </div>

        <div class="squad"></div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Players',
  data() {
    var psg_squad = [
      {num: 1, first_name: 'Alphonse', last_name: 'Areola', position: 'GK'},
      {num: 32, first_name: 'Daniel', last_name: 'Alves', position: 'RB'},
      {num: 2, first_name: 'Thiago', last_name: 'Silva', position: 'CB'},
      {num: 4, first_name: 'Marquinhos', last_name: '', position: 'CB'},
      {num: 21, first_name: 'Layvin', last_name: 'Kurzawa', position: 'LB'},
      {num: 24, first_name: 'Marco', last_name: 'Verratti', position: 'CM'},
      {num: 25, first_name: 'Adrien', last_name: 'Rabiot', position: 'CM'},
      {num: 18, first_name: 'Giovani', last_name: 'Lo Celso', position: 'CM'},
      {num: 7, first_name: 'Angel', last_name: 'Di Maria', position: 'RW'},
      {num: 9, first_name: 'Edinson', last_name: 'Cavani', position: 'ST'},
      {num: 29, first_name: 'Killyan', last_name: 'Mbappe', position: 'LW'},
    ]

    var psg = {
      'name': 'Paris Saint Germain',
      'city': 'Paris',
      'country': 'France',
      'logo': 'logo-psg.png',
      'squad': psg_squad
    }

    var real_squad = [
      {num: 1, first_name: 'Keylor', last_name: 'Navas', position: 'GK'},
      {num: 21, first_name: 'Daniel', last_name: 'Carvajal', position: 'RB'},
      {num: 2, first_name: 'Raphael', last_name: 'Varane', position: 'CB'},
      {num: 4, first_name: 'Sergio', last_name: 'Ramos', position: 'CB'},
      {num: 12, first_name: 'Marcelo', last_name: '', position: 'LB'},
      {num: 18, first_name: 'Casemiro', last_name: '', position: 'CM'},
      {num: 10, first_name: 'Luka', last_name: 'Modric', position: 'CM'},
      {num: 8, first_name: 'Toni', last_name: 'Kroos', position: 'CM'},
      {num: 11, first_name: 'Gareth', last_name: 'Bale', position: 'RW'},
      {num: 9, first_name: 'Karim', last_name: 'Benzema', position: 'ST'},
      {num: 7, first_name: 'Cristiano', last_name: 'Ronaldo', position: 'LW'},
    ]

    var real = {
      'name': 'Club de Futbol Real Madrid',
      'city': 'Madrid',
      'country': 'Spain',
      'logo': 'http://www.gazetaam.com/wp-content/uploads/2014/03/iql2hfa8kks5q78q4ag3.jpeg',
      'squad': real_squad
    }

    return {
      home: psg,
      away: real
    }
  }
}
</script>

<style>
.match {
  position: absolute;
  width: 80%;
  left: 10%;
  border: 1px solid #bebebe;
}

.home {
  float: left;
  background-color: lightsteelblue;
}

.away {
  float: right;
}

.home, .away {
  text-align: left;
  width: 50%;
}

.header{
  margin: 25px;
}

.header img{
  float: right;
  width: 50px;
}

.header span {
  float: left;
  font-size: 30px;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
}

.squad {
  background: green;
  margin: 10px;
  width: 100%;
}
</style>
