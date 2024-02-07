<script>
import { Bar, mixins } from "vue-chartjs";

export default {
  extends: Bar,
  //mixins: [mixins.reactiveProp], houve um erro no module por isso o gráfico não está aparecendo.
  props: {
    chartData: {
      type: Object,
    },
  },
  data() {
    return {
      options: {
        //Chart.js options
        responsive: true,
        maintainAspectRatio: false,
        legend: {
          display: false,
        },
        borderWidth: 0,
        scales: {
          xAxes: [
            {
              stacked: true,
              gridLines: {
                display: false,
              },
            },
          ],
          yAxes: [
            {
              stacked: true,
              ticks: {
                display: false, //this will remove only the label
              },
              gridLines: {
                display: true,
                color: "transparent",
                zeroLineColor: "#66667e",
                zeroLineWidth: 1,
              },
            },
          ],
        },
      },
    };
  },
  mounted() {
    // console.log(this.chartData);
    this.renderChart(this.chartData, this.options);
  },
};
</script>