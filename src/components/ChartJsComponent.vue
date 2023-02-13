<script setup lang="ts">
import { onMounted } from "@vue/runtime-core";
import Chart from "chart.js/auto";

const labels = [
  "January",
  "February",
  "March",
  "April",
  "May",
  "June",
  "July",
  "August",
  "September",
  "October",
  "November",
  "December",
];

const data = {
  labels: labels,
  datasets: [
    {
      label: "My First dataset",
      backgroundColor: "rgb(255, 99, 132)",
      borderColor: "rgb(255, 99 ,132)",
      data: [0, 10, 5, 2, 20, 30, 45, 15, 25, 30, 15, 20, 45],
    },
    {
      label: "My Second dataset",
      backgroundColor: "rgb(20, 50, 90)",
      borderColor: "rgb(10, 40, 80)",
      data: [15, 10, 15, 25, 40, 20, 10, 5, 0, 20, 15, 30],
    },
    {
      label: "My Third dataset",
      backgroundColor: "rgb(34,139,34)",
      borderColor: "rgb(34,139,34)",
      data: [0, 15, 55, 25, 10, 35, 40, 50, 50, 15, 20, 25, 45],
    },
  ],
};

const config = {
  type: "line",
  data: data,
  options: {},
};

onMounted(() => {
  const canvasTag = document.getElementById("myChart");
  const myChart = new Chart(canvasTag, config);
});
</script>

<template>
  <h1>ChartJs</h1>
  <div>
    <canvas id="myChart"></canvas>
  </div>
</template>

<style scoped></style>
