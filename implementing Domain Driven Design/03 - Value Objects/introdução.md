# Objetos de Valor - VOs

Value objects (Objetos de valor) São tipos imutáveis dentro do contexto DDD, dentro do domínio do DDD objetos de valor não tem ID, ou seja, não existem alterações.
Para ilustrar pense em um endereço:

```cs

class Endereco {
  public string Cep {get;}
  public string Logradouro {get;}
  public string Bairro {get;}
  public int Numero {get;}
  public string Complemento {get;}

  public bool ValidateEndereco()
  {
    //TODO: validações
  }
}
```

Outra característica de um objeto de valor é que ele possuí suas próprias validações. Mas de repente você pode pensar, eu prefiro fazer validações diretamente no DTO e o que tem de errado com isso? Eu te explico: vamos citar o exemplo de um middleware de entrada de dados, logo que esses dados entram temos eles sendo tratados e até aí tudo bem, isso geralmente funciona de muito bem, mas tem um problema.

```cs

class EmpresaDto {
  [Required]
  public string Cep {get; set;}

  //TODO: outras validações
}

```

Agora pense que temos ao longo do nosso domínio vários usos de nosso VO Endereço e nem sempre ele vem a partir de uma requisição(Http), podemos recuperar do banco e querer instanciar, ou mesmo após a validação de um middleware ainda vamos instanciar, pense: valor isso gera para o negócio? Validações de domínio tem muito mais valor que validação de propriedades anemicas, no caso de cada instância precisamos assegurar que as validações de domínio ocorrem, é claro que isso é polêmico e inspira pouca produtividade, mas a verdade é que se fizermos as validações no domnínio, ou seja, dentro do VO Endereço vamos assegurar que todas as instâncias desse VO vão ter passada por nosso critério de controle, isso é poderoso.

Um uso comum de um objeto de valor é para uma entidade, veja o exemplo da entidade Empresa utilizando o value object de Endereço

```cs
class Empresa {
  public Guid Id {get;}
  public Endereco Endereco {get;}

  public Empresa(Endereco endereco) {
    Id = Guid.NewId();
    Endereco = endereco;
  }
  // outras props para class empresa

  public bool ValidateEmpresa() {
    //TODO: validações
  }

  //TODO: comportamentos para entidade
}
```

Agora pense que uma empresa x reside em um endereço, concorda que esse endereço não pode ser alterado? Bom, mas você pode pensar, a empresa pode mudar de endereço e isso é um fato, entretanto ela está mudando para outro endereço e o endereço anterior não foi atualizado, pois ele é imutável.

## Resumo

1 - Value objects são imutáveis
2 - Value objects servem entidades
3 - Value objects podem estar contidos em um agregado
4 - Validações sempre devem ocorrer dentro do value object
5 - Se for escrever um set isso não é um value object
6 - Em c# structs combinam com value objects, pois são de natureza imutável
