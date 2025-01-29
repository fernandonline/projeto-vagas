<script>
import BuscarVaga from '@/components/comuns/BuscarVaga.vue'
import IndicadorDetalhes from '@/components/comuns/IndicadorDetalhes.vue'

export default {
  name: 'HomePage',
  components: {
    BuscarVaga,
    IndicadorDetalhes,
  },
}
</script>

<template>
  <div class="container py-4">
    <div class="row">
      <div class="col">
        <buscar-vaga></buscar-vaga>
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
          indicador="14"
          bg="bg-dark"
          color="text-white"
        />
      </div>

    </div>
  </div>
</template>
