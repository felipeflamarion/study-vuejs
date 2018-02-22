<template>
  <div id="app">
    <header>
      Welcome to <br />
      <span>FIFAZZO</span>
    </header>

    <div id="authentication">
      <form method="POST" action=".">
        <input type="text" placeholder="Username"/>
        <input type="password" placeholder="Password"/>
        <input type="submit" value="SIGN IN"/>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #147380;
  margin-top: 60px;
}

#authentication {
  margin: 50px;
}

#authentication form input {
  width: 50%;
  margin-top: 5px;
  height: 30px;
  font-size: 15px;
  text-align: center;
  border-radius: 3px;
  border: 1px solid #4e946d;
}

#authentication form input[type="submit"] {
  background: #4e946d;
  height: 40px;
  color: #fff;
}

#authentication form input[type="submit"]:hover {
  background: #57b380;
  height: 40px;
  color: #fff;
  transition: 200ms;
  cursor: pointer;
}

header {
  font-size: 50px;
}

header span{
  font-size: 100px;
  color: #213133;
  font-weight: bold;
}

.block {
  color: #147380;
  margin: 25px;
}
</style>
