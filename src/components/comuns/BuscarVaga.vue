<script>
export default {
    name: 'BuscarVaga'
}

</script>

<template>
    <div class="h-100 p-5 bg-light border rounded-3">
        <h2> pesquisar vagas</h2>
        <div class="row">
            <div class="col">
                <div class="from-group">
                    <label>titulo da vaga</label>
                    <input type="text" class="form-control"
                        placeholder="Digite palavras chaves como: Desenvolvedor, Analista, etc">
                    <small class="form-text text-muted">Informe palavras que estejam relacionadas com o titulo que você
                        procura</small>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="col">
                <button class="btn btn-outline-dark mt-2" type="button">buscar</button>
            </div>
        </div>
    </div>
</template>