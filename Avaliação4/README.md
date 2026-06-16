# Avaliação Final - Interface Homem-Máquina (IHC)

**Aluno(a):** Guilherme Augusto da Silva Henriques
**Disciplina:** Interação Humano-Computador (IHC)  
**Professora:** Kadidja Valéria  

---

## UA1 – Introdução à IHC e seus benefícios (Desafio 1)

Na interface original, o sistema pergunta: *“Tem certeza de que deseja apagar a entrada do usuario?”*. As opções disponíveis são "Avançar" (posicionada do lado esquerdo) e "Retornar" (posicionada do lado direito).

**Propostas de Melhoria:**
1. **Clareza nos botões:** Mudar o botão "Avançar" para **"Excluir"** e o "Retornar" para **"Cancelar"**. Isso evita ambiguidades sobre a ação que será tomada.
2. **Cores e Affordance (Auto-indicadores):** Utilizar a cor vermelha na opção de "Excluir" para indicar uma ação destrutiva/alerta, e cinza-claro para o botão de "Cancelar", tornando-o uma ação secundária e segura.
3. **Feedback e Contexto:** Modificar o texto da pergunta para que apareça o nome do usuário que será afetado pela ação. Ex: *"Tem certeza de que deseja apagar a entrada de Guilherme?"*.

**Sugestão de Interface Reformulada:**

![Sugestão de Interface Redesenhada](https://storage.googleapis.com/support-kms-prod/g3R2YkikM7sXz28XU2N48a20Jt3NfA2kIq4D)

---

## UA2 – Interface, interação e Affordance (Desafio 2)

**A)** A melhor opção é usar uma interface auditiva focada na compatibilidade com leitores de tela, junto com uma interface de voz. O sistema precisa ter um código bem estruturado por baixo dos panos para que o leitor dite os botões e menus corretamente. Adicionar comandos de voz ajuda o funcionário a fazer o trabalho mais rápido e com total independência.

**B) Equipamentos Necessários:**
* **Teclado padrão:** Essencial para digitação e navegação rápida por atalhos.
* **Headset com microfone:** O fone permite ouvir o leitor de tela com clareza sem atrapalhar os demais colegas no escritório, e o microfone serve para a captação precisa dos comandos de voz.
* **Linha em Braille (Display Braille):** Um equipamento especial de acessibilidade que traduz o texto da tela para pinos em Braille, sendo excelente e indispensável para a leitura de dados complexos com precisão.

---

## UA3 – Storyboarding e prototipação de interfaces (Desafio 3)

**1. Entendimento e Persona:**
Primeiramente, iríamos conversar com o Ricardo para entender o nível da sua perda gradual de visão. Também iríamos mapear a facilidade que ele já tem com os aparelhos que usa no dia a dia, como o smartphone e o relógio inteligente. Com essas informações, criaríamos uma persona bem realista baseada no perfil dele, garantindo que a equipe ficasse perfeitamente alinhada sobre quem é o usuário e suas limitações de locomoção.

**2. Definição da Solução:**
Sabendo que o Ricardo já usa e é apaixonado por tecnologia, a ideia é desenvolver um sistema de navegação em tempo real baseado no Waze. O diferencial é que ele será totalmente controlado por voz através do relógio inteligente, funcionando como uma "Alexa de pulso". Assim, o celular fica seguro no bolso e o Ricardo só precisa falar com o relógio para saber onde está e receber instruções curtas de direção no fone de ouvido, mantendo as mãos livres para a bengala.

**3. Prototipação e Testes:**
Com a ideia definida, partiríamos para os protótipos focados em áudio (Mágico de Oz):
* **Fase 1 (Ambiente Controlado):** Começaríamos de forma simples, onde um integrante da equipe simula as respostas da IA enquanto o Ricardo caminha em um ambiente controlado, para validar se os comandos de voz são claros.
* **Fase 2 (Integração):** Com o fluxo de áudio aprovado, evoluiríamos para o protótipo funcional integrado ao mapa do Waze.
* **Fase 3 (Teste em Campo):** Por fim, faríamos testes reais com o Ricardo na rua, em uma calçada com ruído de trânsito. Essa etapa é fundamental para ajustar a captação do microfone no barulho e calibrar o tempo das instruções, corrigindo problemas antes de fechar o código.

---

## UA4 – TypeScript (Desafio 4)

// ==========================================
// Item A: Classe que representa o Produto
// ==========================================
class Produto {
    // Definição dos 5 atributos solicitados com suas respectivas tipagens
    public nome: string;
    public descricao: string;
    public valorComercial: number;
    public fabricante: string;
    public emEstoque: boolean;

    constructor(
        nome: string, 
        descricao: string, 
        valorComercial: number, 
        fabricante: string, 
        emEstoque: boolean
    ) {
        this.nome = nome;
        this.descricao = descricao;
        this.valorComercial = valorComercial;
        this.fabricante = fabricante;
        this.emEstoque = emEstoque;
    }
}

// ==========================================
// Item B: Classe que gerencia a Venda
// ==========================================
class Venda {
    // Array tipado para aceitar apenas objetos da classe Produto
    public produtos: Produto[];

    constructor(produtos: Produto[]) {
        this.produtos = produtos;
    }

    // Método que percorre a lista de produtos e soma seus valores comerciais
    public calcularTotal(): number {
        let total = 0;
        for (const produto of this.produtos) {
            total += produto.valorComercial;
        }
        return total;
    }
}

## UA4 – TypeScript (Desafio 4)

```typescript
// ==========================================
// Item A: Classe que representa o Produto
// ==========================================
class Produto {
    // Definição dos 5 atributos solicitados com suas respectivas tipagens
    public nome: string;
    public descricao: string;
    public valorComercial: number;
    public fabricante: string;
    public emEstoque: boolean;

    constructor(
        nome: string, 
        descricao: string, 
        valorComercial: number, 
        fabricante: string, 
        emEstoque: boolean
    ) {
        this.nome = nome;
        this.descricao = descricao;
        this.valorComercial = valorComercial;
        this.fabricante = fabricante;
        this.emEstoque = emEstoque;
    }
}

// ==========================================
// Item B: Classe que gerencia a Venda
// ==========================================
class Venda {
    // Array tipado para aceitar apenas objetos da classe Produto
    public produtos: Produto[];

    constructor(produtos: Produto[]) {
        this.produtos = produtos;
    }

    // Método que percorre a lista de produtos e soma seus valores comerciais
    public calcularTotal(): number {
        let total = 0;
        for (const produto of this.produtos) {
            total += produto.valorComercial;
        }
        return total;
    }
}

// ==========================================
// Item C: Instanciação e Demonstração do Fluxo
// ==========================================

// 1. Criando pelo menos dois produtos distintos
const produto1 = new Produto(
    "Cadeira Gamer Pro",
    "Cadeira ergonômica com regulagem de altura e braços 4D",
    1250.00,
    "TechFurniture",
    true
);

const produto2 = new Produto(
    "Mesa Diretor em L",
    "Mesa de escritório em MDF com calha para fiação",
    850.50,
    "OfficeDesign",
    true
);

// 2. Inserindo os produtos criados em um array para a nova venda
const listaDeCompras = [produto1, produto2];
const novaVenda = new Venda(listaDeCompras);

// 3. Executando a soma e exibindo o resultado
const valorTotalVenda = novaVenda.calcularTotal();

console.log("--- Resumo da Venda ---");
console.log(`Produto 1: ${produto1.nome} - R$ ${produto1.valorComercial.toFixed(2)}`);
console.log(`Produto 2: ${produto2.nome} - R$ ${produto2.valorComercial.toFixed(2)}`);
console.log("-----------------------");
console.log(`Valor Total da Venda: R$ ${valorTotalVenda.toFixed(2)}`);
```