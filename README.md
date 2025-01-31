<br />

<div align="center">
    <img src="https://i.imgur.com/pxKDdcY.png" title="source: imgur.com" width="50%"/>
</div>



<br /><br />

## 1. Descrição
<br>
O projeto <b>Vammo</b>Vammo é o desenvolvimento de um backend robusto e escalável para um aplicativo de carona compartilhada. Utilizando TypeScript e o framework NestJS, o sistema visa proporcionar uma experiência eficiente e segura para a administração do catálogo de viagens, usuários e veículos, com foco em facilidade de uso e controle de informações.

## 2. Funcionalidades do projeto
<br>

  2.1 Gerenciamento de Viagens:
  <br>
  Permite adicionar novas viagens ao sistema com as seguintes informações:
  <br>
  - ID
  - Origem
  - Destino
  - Data e hora da ida
  - Preço
  - Distancia entre origem e destino
  - Veículo
  - Status da viagem
  - Nota
<br>
  Consulta de Viagem:
<br>
  - Listagem de todas as viagens.
  - Busca por ID.
  - Visualização de cálculo do tempo da viagem com base na distância e na velocidade média do veículo.
    
  <br>
  Atualização de Viagem:
    <br>
  - Altera a origem, destino, data da ida, preço, distância, veículo, status e nota de uma viagem existente.
  
  <br><br>

  2.2 Gerenciamento de Veículos:
<br>
Permite adicionar novos produtos ao sistema com as seguintes informações:
- ID
- Modelo
- Placa
- Data de fabricação
- Observação
- Disponibilidade
<br>
Consulta de Veículos:
- Busca avançada por modelo, placa e data de fabricação, observação e disponibilidade.
- Visualização detalhada do perfil de um veículo.
<br>
Atualização de Dados:
- Alterar modelo, placa, data de fabricação, observação e disponibilidade.
<br><br>

2.3 Gerenciamento de Usuários:
<br>
  Permite adicionar novos usuários ao sistema com as seguintes informações:
  <br>
  - ID
  - Tipo de usuário
  - Genero
  - Nome
  - Data de Nascimento
  - Usuário
  - Senha
  - Foto
  - Avaliação
  <br>
  Consulta de Usuários:
<br>
  - Busca avançada por nome e usuário.
  - Visualização detalhada do perfil de um usuário.
  <br>
  Atualização de Dados:
<br>
  - Alterar informações cadastrais, como nome, usuário ou foto.

  
------

<br>

## 2. Sobre esta API

<strong>Nest (NestJS)</strong> é uma estrutura para a construção de aplicativos Node.js do lado do servidor eficientes e escalonáveis. Ele usa JavaScript progressivo, é construído e oferece suporte total a TypeScript (mas ainda permite que os desenvolvedores codifiquem em JavaScript puro) e combina elementos de OOP (Programação Orientada a Objetos), FP (Programação Funcional) e FRP (Programação Funcional Reativa).
Nos bastidores, o Nest faz uso de estruturas robustas de servidor HTTP como o Express (o padrão) e, opcionalmente, pode ser configurado para usar o Fastify também!

O Nest fornece um nível de abstração acima desses Node.js comuns frameworks (Express/Fastify), mas também expõe suas APIs diretamente ao desenvolvedor. Isso dá aos desenvolvedores a liberdade de usar uma infinidade de módulos de terceiros disponíveis para a plataforma subjacente.
<br><br>

### 2.1. Principais Funcionalidades
<br>
- Estrutura Modular
- Suporte a TypeScript
- Injeção de dependências
- Testes facilitados
- Controlleres e Rotas
- Validação e serialização
- Integração com bibliotecas externas


------

<br><br>

## 3. Diagrama de Classes

# 

---

```mermaid
---
config:
  theme: dark
  layout: dagre
---

classDiagram
    class Categoria {
        id: number
        nome: string
        descricao: string
        produto: Produto[]
    }

    class Produto {
        id: number
        nome: string
        preco: number
        foto: string
        informacoes: string
        categoria: Categoria
        usuario: Usuario
    }

    class Usuario {
        id: number
        nome: string
        usuario: string
        senha: string
        foto: string
        produto: Produto[]
    }

    Categoria "1" --> "many" Produto : contém
    Produto "many" --> "1" Categoria : pertence a
    Produto "many" --> "1" Usuario : criado por
    Usuario "1" --> "many" Produto : possui
```

------

<br>

## 4. Diagrama Entidade-Relacionamento (DER)



<div align="center">
    <img src="https://i.imgur.com/NZ7cDkA.png" title="DER">
</div>




------

<br>

## 5. Tecnologias utilizadas

| Item                          | Descrição  |
| ----------------------------- | ---------- |
| **Servidor**                  | Node JS    |
| **Linguagem de programação**  | TypeScript |
| **Framework**                 | Nest JS    |
| **ORM**                       | TypeORM    |
| **Banco de dados Relacional** | MySQL      |
| **Deploy**                    | Swagger    |
|                               | Render     |

------

<br>

## 6. Configuração e Execução

1. Clone o repositório
2. Instale as dependências: `npm install`
3. Configure o banco de dados no arquivo `app.module.ts`
4. Execute a aplicação: `npm run start:dev`

------

<br>

## 7. Colaboradores

`@ZarathosFreya`
`@Beatriz-Rodrigues-P`
`@brunop-lima`
`@emilyestvz`
`@fern-menezes`
`@Josadack`
`@VictorPestana`
