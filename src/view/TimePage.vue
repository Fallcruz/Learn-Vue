<template>
  <!-- Navigation -->
  <div class="navbar" id="navbar">
    <a href="#">Time</a>
    <a href="#">Stopwatch</a>
  </div>
  <!-- End Navigation -->

  <div class="container-fluid main">
    <h3 class="mb-4">Time is running</h3>
    <!-- Content -->
    <div class="container col-8 content d-flex justify-content-around align-items-center">
      <div class="col-3 boxTime">
        <p id="hours">00</p>
      </div>
      <p>:</p>
      <div class="col-3 boxTime">
        <p id="minutes">00</p>
      </div>
      <p>:</p>
      <div class="col-3 boxTime">
        <p id="seconds">00</p>
      </div>
    </div>
    <!-- End Content -->

    <!-- Full Screen -->
    <!-- <div class="container col-2 d-flex mt-4 text-center">
      <div class="circle mx-auto">
        <i class="fa-solid fa-expand expand" id="fullScreen"></i>
      </div>
      <div class="circle mx-auto">
        <i class="fa-solid fa-compress expand" id="smallScreen"></i>
      </div>
    </div> -->
    <!-- End Full Screen -->
  </div>
</template>

<script>
export default {
  name: 'TimePage'
}
const currentTime = () => {
  var hours = document.getElementById("hours");
  var minutes = document.getElementById("minutes");
  var seconds = document.getElementById("seconds");

  let date = new Date();
  let hh = date.getHours();
  let mm = date.getMinutes();
  let ss = date.getSeconds();
  
  hh = hh < 10 ? `0${hh}` : hh;
  mm = mm < 10 ? `0${mm}` : mm;
  ss = ss < 10 ? `0${ss}` : ss;

  hours.innerHTML = hh;
  minutes.innerHTML = mm;
  seconds.innerHTML = ss;
  
  let mySound = new Audio('sound/tick.wav');
  mySound.play();
};

currentTime();
setInterval(currentTime, 1000);

</script>


<style>
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
  background-image: url("../assets/bg-1.jpg");
  background-size: cover;
  /* background-position: center; */
  height: 100vh;
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