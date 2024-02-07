<template>

<div id="grafico">
    <div>
      <h1>Gráfico de Barras</h1>
      <bar-chart :chart-data="chart1Data"></bar-chart>
    </div>
  </div>

</template>

<script>
     
  import axios from "axios";
  import BarChart from "./BarChart.vue";

  export default {

    name: "CountryGraph",
    
    components: {
    BarChart,
  },
  data() {
    return {
      chart1Data: {},
      loaded: false,
      country: 0,
      confirmed: 0,
      deaths: 0,
    };
  },
  created() {
    this.fillData();
  },
  mounted() {
    this.fillData();
  },
  watch() {
    this.fillData();
  },
  methods: {
    fillData() {
      axios
        .get("https://covid19-brazil-api.now.sh/api/report/v1/countries")
        .then((response) => {
          //set loaded to true (important for initial load)
          this.loaded = true;

          //Chart4 Data
          this.country = response.data.bpi.USD.rate_float;
          this.confirmed = response.data.bpi.USD.rate_float + 20000;
          this.deaths = response.data.bpi.USD.rate_float + 10000;
          this.chart1Data = {
            labels: ["Países", "Confirmados"],
            datasets: [
              {
                label: "País",
                backgroundColor: "#333353",
                data: [this.country],
              },
              {
                label: "Confirmados",
                backgroundColor: "#00597d",
                data: [this.confirmed],
              },
              {
                label: "Mortos",
                backgroundColor: "#00d7a0",
                data: [0, this.deaths],
              },
            ],
          };
        })
        .catch((error) => {
          console.error(error);
        });
    },
  },
  computed: {
    getCountry: {
      get: function () {
        return this.country;
      },
    },
    getConfirmed: {
      get: function () {
        return this.confirmed;
      },
    },
    getDeaths: {
      get: function () {
        return this.deaths;
      },
    },
  },
  }
</script>