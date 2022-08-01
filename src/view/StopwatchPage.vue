<template>
  <!-- Navigation -->
  <div class="navbar" id="navbar">
    <a href="index.html">Time</a>
    <a href="stopwatch.html">Stopwatch</a>
  </div>
  <!-- End Navigation -->

  <div class="container-fluid main">
    <h3 class="mb-4">Stopwatch</h3>
    <!-- Content -->
    <div class="container col-8 content d-flex justify-content-between align-items-center">
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
      <p>:</p>
      <div class="col-3 boxTime">
        <p id="tens">00</p>
      </div>
    </div>
    <!-- End Content -->

    <!-- Full Screen -->
    <div class="container col-3 d-flex mt-4 text-center">
      <div class="circle mx-auto">
        <i class="fa-solid fa-play expand" onclick="Start()"></i>
      </div>
      <div class="circle mx-auto">
        <i class="fa-solid fa-pause expand" onclick="Stop()"></i>
      </div>
      <div class="circle mx-auto">
        <i class="fa-solid fa-trash expand" onclick="Clear()"></i>
      </div>
    </div>
    <!-- End Full Screen -->
  </div>
</template>

<script>
export default {
  name: 'StopwatchPage'
}
</script>