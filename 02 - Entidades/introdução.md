# Entidades

Antes de iniciar com entidades você precisa saber, Entidades do banco não são Entidades em DDD e sim em um software que usa DDD é comum ter Arquivos como:

Entidade rica

```cs
class Pessoa {
  public Guid Id;
  public string Nome;

  public bool ValidatePessoa() {

  }

  //TODO: comportamentos
}

```

Entidade anemica

```cs
class Pessoa {
  public Guid Id {get;set;};
  public string Nome {get;set};

  // segue estritamente o modelo anemico do banco de dados, geralmente não tem comportamento rico

  //TODOL: alguma implementação específica para o ORM
}

```

...continua.....
