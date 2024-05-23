<template>
    <div>
      <canvas :id="id" width = "250" height=" 200"></canvas>
    </div>
  </template>
  
  <script setup>
  import { onMounted, defineProps } from 'vue';
  import Chart from 'chart.js/auto';
  
  const props = defineProps(["id" ,"datasets","labels"]);
  
  const labels = [
    'January',
    'February',
    'March',
    'April',
    'May',
    'June',
  ];
  
  const data = {
    labels: props.labels || labels,
    datasets: props.datasets || [{
      label: 'My First dataset',
      backgroundColor: 'rgb(255, 99, 132)',
      borderColor: 'rgb(255, 99, 132)',
      data: [0, 10, 5, 2, 20, 30, 45],
      tension: 0.5,
    }]
  };
  
  const config = {
    type: 'line',
    data: data,
    options: {}
  };
  
  onMounted(() => {
    new Chart(document.getElementById(props.id), config);
  });
  </script>
  