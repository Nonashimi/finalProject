  <template>
    <div class="all">
      <div class="Limit">{{ limit }}</div>
      <div class="circl">
        <canvas ref="chartCanvas" width="110" height="110"></canvas>
        <div class="proc">{{ data }}%</div>
      </div>
    </div>
          
  </template>
  
  <script>
  export default {
    props: {
      data: {
        type: Number,
        required: true,
      },
      color:{
      type:String,
      default:"#428777"
      },
      max: {
        type: Number,
        default: 100,
      },
      limit:String,
    },
    mounted() {
      this.drawChart();
    },
    watch: {
      data: 'drawChart',
    },
    methods: {
      drawChart() {
        const canvas = this.$refs.chartCanvas;
        const ctx = canvas.getContext('2d');
  
        ctx.clearRect(0, 0, canvas.width, canvas.height);
  
        const centerX = canvas.width/ 2;
        const centerY = canvas.height / 2;
        const radius = canvas.width / 2 - 10; 
  
        ctx.beginPath();
        ctx.arc(centerX, centerY, radius, 0,  2* Math.PI);
        ctx.strokeStyle = 'rgba(230, 234, 240, 0.758)';
        ctx.lineWidth = 15;
        ctx.stroke();
  
        const progress = (this.data / this.max) * 2 * Math.PI;
        ctx.beginPath();
        ctx.arc(centerX, centerY, radius, +Math.PI / 2, +Math.PI / 2 + progress);
        ctx.strokeStyle = this.color; 
        ctx.lineWidth = 15;
        ctx.stroke();
      },
    },
  };
  </script>
  
  <style scoped>
  .circl{
    position: relative;
  }
  .all{
    width:110px;
  }
  .proc{
    position: absolute;
    top: 37%;
    left: 35%;
    font-weight: 600;
  }
  .Limit{
    text-align: center;
    font-weight: 700;
    margin-bottom: 5px;
    font-size: 16px;
  }
  </style>
  