<template>
  <div class="body">
    <!-- Navigation -->
    <div class="navbar" id="navbar">
      <a href="index.html">Time</a>
      <a href="stopwatch.html">Stopwatch</a>
    </div>
    <!-- End Navigation -->
  </div>
</template>

<script>
export default {
  name: 'TimePage'
}
</script>

<style>
.body {
  background-image: url("../assets/bg-1.jpg");
  background-size: cover;
  height: 100vh;
}
.navbar {
  position: absolute;
  left: 6%;
  top: 5%;
}
.navbar a {
  font-family: 'Rubik', sans-serif;
  text-decoration: none;
  color: black;
  margin: 0 15px !important;
}
.navbar a:hover {
  color: grey;
}
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.main h3 {
  font-family: 'Rubik', sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  letter-spacing: 10px;
}
.content p {
  font-size: 7vw;
  font-family: 'Rubik', sans-serif;
  font-weight: 500;
  margin: 0;
}
.boxTime {
  height: 150px;
  backdrop-filter: blur(3px);
  border-radius: 10px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.circle {
  width: 60px;
  height: 60px;
  backdrop-filter: blur(3px);
  box-shadow: rgba(50, 50, 93, 0.25) 0px 6px 12px -2px, rgba(0, 0, 0, 0.3) 0px 3px 7px -3px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.circle .expand {
  width: 20px;
  height: 20px;
  cursor: pointer;
  transition: 0.2s;
}
.circle:hover .expand {
  color: whitesmoke;
  width: 30px;
  height: 30px;
}
</style>