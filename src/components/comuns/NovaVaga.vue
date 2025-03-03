<template>
    <div class="card">
        <div class="card-header bg-dark text-white"> {{ titulo }} </div>
        <div class="card-body">
            <p> {{ descricao }} </p>
        </div>
        <div class="card-footer">
            <small class="text-muted">
                Salario: R$ {{ salario }} |
                Modalidade: {{ modalidade }} |
                Tipo: {{ tipo }} |
                Publicado em: {{ publicacao }}
            </small>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NovaVaga',
    props: [
        'titulo',
        'descricao',
        'salario',
        'modalidade',
        'tipo',
        'publicacao'
    ],
}
</script>