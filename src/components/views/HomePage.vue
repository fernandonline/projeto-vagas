<script>
import BuscarVaga from '@/components/comuns/BuscarVaga.vue'
import IndicadorDetalhes from '@/components/comuns/IndicadorDetalhes.vue'
import NovaVaga from '@/components/comuns/NovaVaga.vue'

export default {
  name: 'HomePage',
  components: {
    BuscarVaga,
    IndicadorDetalhes,
    NovaVaga,
  },
  data: () => ({
    usuariosOnline: 14,

    vagas: [
      {
        titulo: 'Analista Programador PHP Pleno',
        descricao: 'Profissional com conhecimentos em PHP, Laravel e MySQL. Necessário 3 anos de experiências. Atuará na manutenção de sistemas legados da empresa.',
        salario: 6000,
        modalidade: 'Home Office',
        tipo: 'PJ',
        publicacao: '2021-10-10'
      },
      {
        titulo: 'Programador JavaScript Angular',
        descricao: 'Profissional com conhecimentos avançados em JavaScript e Angular.',
        salario: 5000,
        modalidade: 'Presencial',
        tipo: 'CLT',
        publicacao: '2021-10-07'
      },
      {
        titulo: 'Programador JavaScript Vue',
        descricao: 'Profissional com conhecimentos avançados em JavaScript e Vue.',
        salario: 5000,
        modalidade: 'Home Office',
        tipo: 'CLT',
        publicacao: '2021-10-06'
      },
      {
        titulo: 'Analista de Banco de Dados Sênior',
        descricao: 'Domínio dos bancos de dados SQL Server, Oracle, Postgre e MySQL',
        salario: 9000,
        modalidade: 'Presencial',
        tipo: 'PJ',
        publicacao: '2021-10-06'
      },
      {
        titulo: 'Programador Web Júnior',
        descricao: 'Conhecimentos básicos em HTML, CSS, JavaScript, Bootstrap, PHP e MySQL',
        salario: 3000,
        modalidade: 'Presencial',
        tipo: 'CLT',
        publicacao: '2021-10-05'
      }
    ],

  }),
  methods: {
    getUsuariosOnline() {
      this.usuariosOnline = Math.floor(Math.random() * 101)
    }
  },
  created() {
    setInterval(this.getUsuariosOnline, 10000)
  }
}
</script>

<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <buscar-vaga></buscar-vaga>
      </div>
    </div>

    <div class="row mt-5" v-for="(vaga, index) in vagas" :key="index">
      <div class="col">
        <nova-vaga
          :titulo="vaga.titulo"
          :descricao="vaga.descricao"
          :salario="vaga.salario"
          :modalidade="vaga.modalidade"
          :tipo="vaga.tipo"
          :publicacao="vaga.publicacao"
        />
      </div>
    </div>
    
    <div class="row mt-5">

      <div class="col-4">
        <indicador-detalhes 
          titulo="Vagas abertas"
          indicador="104"
          bg="bg-dark"
          color="text-white"
        />
      </div>

      <div class="col-4">
        <indicador-detalhes 
          titulo="Profissionais cadastrados"
          indicador="125"
          bg="bg-white"
          color="text-dark"
        />
      </div>

      <div class="col-4">
        <indicador-detalhes 
          titulo="Visitantes online"
          :indicador="usuariosOnline"
          bg="bg-dark"
          color="text-white"
        />
      </div>

    </div>
  </div>
</template>
