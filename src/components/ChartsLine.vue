<template>
  <div>
    <canvas ref="lineChartCanvas" width="250" height="200"></canvas>
  </div>
</template>

<script>
export default {
  data() {
    return {
      chartData: [10, 20, 40, 20, 40, 60, 40, 60, 80, 60],
    };
  },
  mounted() {
    this.drawChart();
  },
  watch: {
    chartData: 'drawChart',
  },
  methods: {
    drawChart() {
      const canvas = this.$refs.lineChartCanvas;
      const ctx = canvas.getContext('2d');

      ctx.clearRect(0, 0, canvas.width, canvas.height);

      const margin = 20;
      const chartWidth = canvas.width - 2 * margin;
      const chartHeight = canvas.height - 2 * margin;

      ctx.beginPath();
      ctx.moveTo(margin, margin);
      ctx.lineTo(margin, canvas.height - margin);
      ctx.lineTo(canvas.width - margin, canvas.height - margin);
      ctx.stroke();

      const interval = chartWidth / (this.chartData.length - 1);

      let prevY;

      for (let i = 0; i < this.chartData.length; i++) {
        const x = margin + i * interval;
        const y = canvas.height - margin - (chartHeight * this.chartData[i]) / 100;

        ctx.beginPath();
        ctx.arc(x, y, 5, 0, 2 * Math.PI);
        ctx.fillStyle = 'blue';
        ctx.fill();

        if (i > 0) {
          // Используйте кривые Безье для более круглых линий
          const prevX = margin + (i - 1) * interval;
          const controlPointX = (prevX + x) / 2;

          ctx.beginPath();
          ctx.moveTo(prevX, prevY);
          ctx.quadraticCurveTo(controlPointX, prevY, x, y);
          ctx.strokeStyle = 'blue';
          ctx.stroke();
        }

        prevY = y;
      }
    },
  },
};
</script>

<style scoped>
</style>
