

<template>

 <br><br>

<h1 class="text-2xl font-bold tracking-tight sm:text-2xl"> Lista casos por todos estados brasileiros </h1>

<div class="flex flex-col">
        <div class="overflow-x-auto">
            <div class="p-1.5 w-full inline-block align-middle">
                <div class="overflow-hidden border rounded-lg">
                    <table class="min-w-full divide-y divide-gray-200">
                        <thead class="bg-gray-50">
                         


                          <tr>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Estado</th>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Casos</th>
                        <th
                        scope="col"
                        class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Mortes</th>
                        </tr>
                        </thead>

                        <tbody>
                        <tr v-for="item in report">
                          <td> {{ item.state }}</td>
                          <td> {{ item.cases }}</td>
                          <td> {{ item.deaths }}</td>
                        </tr>
                        </tbody>


                        </table>
                </div>
            </div>
        </div>
</div>

<br><br>

<h1 class="text-2xl font-bold tracking-tight sm:text-2xl"> Lista casos por estado brasileiro </h1>

<div class="flex flex-col">
        <div class="overflow-x-auto">
            <div class="p-1.5 w-full inline-block align-middle">
                <div class="overflow-hidden border rounded-lg">
                    <table class="min-w-full divide-y divide-gray-200">
                        <thead class="bg-gray-50">
                         


                          <tr>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Estado</th>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Casos</th>
                        <th
                        scope="col"
                        class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Mortes</th>
                        </tr>
                        </thead>

                        <tbody>
                        <tr>
                          <td> {{ estado.state }}</td>
                          <td> {{ estado.cases }}</td>
                          <td> {{ estado.deaths }}</td>
                        </tr>
                        </tbody>


                        </table>
                </div>
            </div>
        </div>
</div>


<br><br>

<h1 class="text-2xl font-bold tracking-tight sm:text-2xl"> Lista casos no brasil em data específica. </h1>



<div class="flex flex-col">
        <div class="overflow-x-auto">
            <div class="p-1.5 w-full inline-block align-middle">
                <div class="overflow-hidden border rounded-lg">
                    <table class="min-w-full divide-y divide-gray-200">
                        <thead class="bg-gray-50">
                         


                          <tr>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Estado</th>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Casos</th>
                        <th
                        scope="col"
                        class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Mortes</th>
                        </tr>
                        </thead>

                        <tbody>
                         
                          <tr v-for="item in dataEspecifica">
                          <td> {{ item.state }}</td>
                          <td> {{ item.cases }}</td>
                          <td> {{ item.deaths }}</td>
                         
                        </tr>
                        </tbody>


                        </table>
                </div>
            </div>
        </div>
</div>


<br><br>

<h1 class="text-2xl font-bold tracking-tight sm:text-2xl"> Lista casos por país </h1>

<div class="flex flex-col">
        <div class="overflow-x-auto">
            <div class="p-1.5 w-full inline-block align-middle">
                <div class="overflow-hidden border rounded-lg">
                    <table class="min-w-full divide-y divide-gray-200">
                        <thead class="bg-gray-50">
                         


                          <tr>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >País</th>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >confirmados</th>
                        <th
                        scope="col"
                        class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Mortes</th>
                        </tr>
                        </thead>

                        <tbody>
                         
                          <tr v-for="item in pais">
                          <td> {{ item.country }}</td>
                          <td> {{ item.confirmed }}</td>
                          <td> {{ item.deaths }}</td>
                         
                        </tr>
                        </tbody>


                        </table>
                </div>
            </div>
        </div>
</div>


<br><br>

<h1 class="text-2xl font-bold tracking-tight sm:text-2xl"> Lista casos por países </h1>


<div class="flex flex-col">
        <div class="overflow-x-auto">
            <div class="p-1.5 w-full inline-block align-middle">
                <div class="overflow-hidden border rounded-lg">
                    <table class="min-w-full divide-y divide-gray-200">
                        <thead class="bg-gray-50">
                         


                          <tr>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >País</th>
                        <th
                        scope="col"
                       class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >confirmados</th>
                        <th
                        scope="col"
                        class="px-6 py-3 text-xs font-bold text-left text-gray-500 uppercase"
                        >Mortes</th>
                        </tr>
                        </thead>

                        <tbody>
                         
                          <tr v-for="item in paises">
                          <td> {{ item.country }}</td>
                          <td> {{ item.confirmed }}</td>
                          <td> {{ item.deaths }}</td>
                         
                        </tr>
                        </tbody>


                        </table>
                </div>
            </div>
        </div>
</div>


<br><br>

<h1 class="text-2xl font-bold tracking-tight sm:text-2xl"> Consultar status da API </h1>

Status: {{ statusApi.status  }}
<br>
Ambiente: {{ statusApi.environment }}

<br><br>

<country-graph></country-graph>

</template>

<script>
     
  //import CountryGraph from "./components/CountryGraph.vue";

  export default {

   /* name: "app",
  components: {
    CountryGraph,
  },*/

  data() {
    return {
      report: [],
      estado: [],
      dataEspecifica: [],
      pais: [],
      paises: [],
      statusApi: []
    }
  },
  methods: {
    getReport() {
      fetch('https://covid19-brazil-api.now.sh/api/report/v1')
        .then(response => response.json())
        .then(data => this.report = data.data)
    },

    getEstado() {
      fetch('https://covid19-brazil-api.now.sh/api/report/v1/brazil/uf/sp')
        .then(response => response.json())
        .then(data => this.estado = data)
    },

    getDataEspecifica() {
      fetch('https://covid19-brazil-api.now.sh/api/report/v1/brazil/20200318')
        .then(response => response.json())
        .then(data => this.dataEspecifica = data.data)
    },
    
    getPais() {
      fetch('https://covid19-brazil-api.now.sh/api/report/v1/brazil')
        .then(response => response.json())
        .then(data => this.pais = data)
    },

    getPaises() {
      fetch('https://covid19-brazil-api.now.sh/api/report/v1/countries')
        .then(response => response.json())
        .then(data => this.paises = data.data)
    },

    getStatusApi() {
      fetch('https://covid19-brazil-api.now.sh/api/status/v1')
        .then(response => response.json())
        .then(data => this.statusApi = data)
    }

    

  },
  mounted() {
    this.getReport(),
    this.getEstado(),
    this.getDataEspecifica(),
    this.getPais(),
    this.getPaises(),
    this.getStatusApi()
  }

 

}

</script>