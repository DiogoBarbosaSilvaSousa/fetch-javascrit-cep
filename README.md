# Começando com fetch no Javascript

Atualmente a pessoa que fez a compra precisa preencher todos os campos de maneira correta para que haja validação e a compra seja finalizada com sucesso.

Porém, pode ser que alguns dos campos seja digitado de maneira incorreta resultando em um endereço errado. Sendo assim teremos problemas na validação, finalização da compra e o descontentamento do cliente em relação a loja pois não conseguiu efetuar a finalização da compra.

# Automatizando

Para automatizar o preenchimento iremos usar o Javascript, vamos primeiro ver como o HTML está definindo e pegar o atributo do button pelo Javascript.

```
<div class="container col-md-5">
      <form>
        <div class="form-group font-weight-bold">
          <label>CEP</label>
          <input type="text" id="cep" pattern= "\d{5}-?\d{3}" class="form-control" required placeholder="Insira o seu CEP">
        </div>
        <div class="form-group font-weight-bold">
          <label>Rua</label>
          <input type="text" class="form-control" id="rua" placeholder="...">
        </div>
        <div class="form-group font-weight-bold">
          <label>Complemento</label>
          <input type="text" class="form-control" id="complemento" placeholder="...">
        </div>
        <div class="form-group font-weight-bold">
          <label>Bairro</label>
          <input type="text" class="form-control" id="bairro" placeholder="...">
        </div>
        <div class="form-group font-weight-bold">
          <label>Cidade</label>
          <input type="text" class="form-control" id="cidade" placeholder="...">
        </div>
        <div class="form-group font-weight-bold">
          <label>Estado</label>
          <input type="text" class="form-control" id="estado" placeholder="...">
        </div>
        <button type="submit" id="btnPesquisar" class="btn btn-primary">Pesquisa</button>
        <button type="button" id="btnLimpar" class="btn btn-danger">Limpar</button>
      </form>
  </div>

```

No Javascript vai ficar assim:

```
const btnPesquisarCEP = document.querySelector("#btnPesquisar");
```

Com isto feito, adicionamos um evento de click do botão usando arrow function:

```

btnPesquisarCEP.addEventListener("click", event =>{}

```