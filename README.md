# HTTP

## Índice

1. [HTTP em poucas palavras](#http-em-poucas-palavras)
2. [Portas padrões](#portas-padrões)
3. [Corpo de uma requisição](#corpo-de-uma-requisição)
4. [URI (Uniform Resource Identifier)](#uri-(uniform-resource-identifier))
5. [Mêtodos HTTP](#mêtodos-http)
      - [GET](#get)
      - [HEAD](#head)
      - [POST](#post)
      - [PUT](#put)
      - [DELETE](#delete)
      - [TRACE](#trace)
      - [OPTIONS](#options)
      - [PATCH](#patch)
      - [CONECT](#conect)

## HTTP em poucas palavras

- http segue o modelo de request-response
- http é stateless (cada requisição é unica!)
- uma requisição precisa de todas as informações para gerar respostas
- sessões (cookies)

## Portas padrões

- http => 80
- https => 443

## Corpo de uma requisição

```https://www.meusite.com.br:443/corpo-de-um-http```

- Protocolo => `https`
- Web => `www`
- Dominio => `www.meusite.com.br`
- Tipo => `.com`
- Pais => `.br`
- Porta => `443`
- Recurso => `/corpo-de-um-http`

## URI (Uniform Resource Identifier)

- Uma URL (Uniform Resource Locator) é uma URI. No contexto do desenvolvimento web, ambas as siglas são válidas para falar de endereços na web. As siglas são praticamente sinônimos e são utilizadas dessa forma.

- Uma URL é uma URI, mas nem todas as URI's são URL's! Existem URI's que identificam um recurso sem definir o endereço, nem o protocolo. Em outras palavras, uma URL representa uma identificação de um recurso (URI) através do endereço, mas nem todas as identificações são URL's.

- URI pode ser uma URL ou um URN (Uniform Resource Name).

## Mêtodos HTTP

### GET

O método GET requisita uma representação do recurso especificado. Requisições usando GET devem apenas recuperar dados e não devem ter qualquer outro efeito. (Isto também é verdade para alguns outros métodos HTTP.) O W3C publicou princípios de orientações sobre esta distinção, "O projeto de aplicações web devem ser informados pelos princípios acima, mas também por limitações relevantes."

### HEAD

Variação do GET em que o recurso não é retornado. É usado para obter metainformações por meio do cabeçalho da resposta, sem ter que recuperar todo o conteúdo.

### POST

Envia dados para serem processados (por exemplo, dados de um formulário HTML) para o recurso especificado. Os dados são incluídos no corpo do comando. Sua utilização em uma requisição ocorre quando é necessário enviar dados ao servidor para serem processados, geralmente por um programa script identificado no Request-URI. Uma requisição por meio desse método sempre requer que as informações submetidas sejam incluídas no corpo da mensagem e formatadas como uma query string, além de conter cabeçalhos adicionais especificando seu tamanho (Content-Length) e seu formato (Content-Type). Por isso, esse método oferece uma maior segurança em relação aos dados transferidos, ao contrário do método GET que os dados são anexados a URL, ficando visíveis ao usuário.

### PUT

O método PUT envia os dados de forma semelhante ao POST, através do corpo do HTTP a diferença entre os 2 métodos é semântica. Por exemplo:

Caso você necessite atualizar os dados de um usuário, utilizando o método PUT você pode os atualizar diversas vezes, pois o PUT vai sobrescrever os dados com isso ficará somente com um único registro atualizado.

Se você executasse este mesmo procedimento utilizando o método POST, você criaria diversos registros para cada requisição realizada.

### DELETE

Exclui o recurso.

### TRACE

Ecoa o pedido, de maneira que o cliente possa saber o que os servidores intermediários estão mudando em seu pedido.

### OPTIONS

Recupera os métodos HTTP que o servidor aceita.

### PATCH

Serve para atualizar partes de um recurso, e não o recurso todo.

### CONECT

Serve para uso com um proxy que possa se tornar um túnel SSL e TLS (um túnel pode ser usado, por exemplo, para criar uma conexão segura).
