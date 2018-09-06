# Data Driven Testing
O Data-driven é uma estrutura de automação de testes que armazena dados de teste em uma tabela ou no formato de planilha distribuída. Isso permite que os engenheiros de automação tenham um único script de teste que possa executar testes para todos os dados de teste na tabela. Neste projeto foi utilizado o DDT para o report de issues e suas variações.

Criação de uma função com retorno de uma lista de TestCaseData
```sh
public static List<TestCaseData> InsercaoIssues {}
 ```
 Criação de uma lista de TestCaseData
 ```sh
 var testCases = new List<TestCaseData>();
```
Preenchimento da lista de TesteCaseData com TesteCase 
```sh
var testCase = new TestCaseData(category, reproducibility, severity, priority, summary, description);
                                testCases.Add(testCase);
```

Criação do Teste recebendo um TesteCaseSource referente à lista retornada pelo InsercaoIssues e seus parâmetros
```sh
[Category("DataDriven"), TestCaseSource("InsercaoIssues")]
        public void Issue_DD_InsertSimple(string category, string reproducibility, string severity, string priority, string summary, string description)
        {}
```
