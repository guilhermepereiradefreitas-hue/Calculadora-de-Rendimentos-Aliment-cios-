# 📊 Calculadora de Rendimento Alimentício

![Versão](https://img.shields.io/badge/versão-3.0.0-blue.svg)
![Licença](https://img.shields.io/badge/licença-MIT-green.svg)
![Status](https://img.shields.io/badge/status-ativo-success.svg)

## 📝 Descrição

Calculadora profissional de rendimento de produtos alimentícios desenvolvida para auxiliar na gestão de custos e análise de perdas em estabelecimentos gastronômicos, cozinhas industriais e gestores de alimentos.

A aplicação permite calcular automaticamente o custo real dos produtos considerando o percentual de rendimento após o processamento OU o número de unidades produzidas, fornecendo dados precisos sobre custos brutos, líquidos, perdas financeiras e custo por unidade.

## ✨ Funcionalidades

### Versão 3.0.0 (Atual) - NOVO! 🎉
- ✅ **Dois Modos de Cálculo**:
  - 📊 **Por Rendimento (%)**: Calcula baseado no percentual de aproveitamento
  - 🔢 **Por Unidades**: Calcula baseado na quantidade de produtos finais
- ✅ **Custo por Unidade**: Cálculo automático do custo individual de cada produto
- ✅ **Rendimento Opcional**: Não é mais obrigatório preencher o rendimento
- ✅ **Badges Visuais**: Identificação clara do tipo de cálculo usado
- ✅ **Exportação Completa**: Excel inclui todos os novos campos

### Versão 2.0.0
- ✅ Exportação para Excel com formatação profissional
- ✅ Download de README
- ✅ Campo para logo personalizável
- ✅ Créditos do criador

### Versão 1.0.0
- ✅ Cadastro básico de produtos
- ✅ Cálculos de rendimento
- ✅ Tabela de visualização
- ✅ Resumo de totais

## 🚀 Como Usar

### 1. Escolher Modo de Cálculo
Escolha entre dois modos:
- **📊 Cálculo por Rendimento (%)**: Para produtos com perda de peso/volume
- **🔢 Cálculo por Unidades**: Para produtos que geram unidades contáveis

### 2. Adicionar Produtos

#### Modo Rendimento (%):
1. Preencha o nome do produto (ex: "Carne Bovina")
2. Informe a quantidade em kg (ex: 5.00)
3. Digite o preço por kg em R$ (ex: 35.00)
4. Insira o percentual de rendimento (ex: 75%) - OPCIONAL
5. Clique em "➕ Adicionar Produto"

**Exemplo**: 5kg de carne a R$ 35/kg com 75% de rendimento
- Custo Total: R$ 175,00
- Custo Líquido: R$ 131,25 (75% de R$ 175)
- Perda: R$ 43,75

#### Modo Unidades:
1. Preencha o nome do produto (ex: "Bolo de Chocolate")
2. Informe a quantidade em kg (ex: 2.50)
3. Digite o preço por kg em R$ (ex: 15.00)
4. Insira quantas unidades foram produzidas (ex: 12)
5. Clique em "➕ Adicionar Produto"

**Exemplo**: 2.5kg de ingredientes a R$ 15/kg gerando 12 bolos
- Custo Total: R$ 37,50
- Custo Líquido: R$ 37,50
- Custo por Unidade: R$ 3,13
- Perda: R$ 0,00

### 3. Visualizar Dados
- A tabela mostra todos os produtos com badges identificando o tipo
- O resumo exibe totais consolidados
- Coluna "Custo/Unidade" mostra o valor individual (quando aplicável)

### 4. Exportar para Excel
1. Clique no botão "📥 Exportar para Excel"
2. O arquivo inclui todos os campos: tipo, rendimento/unidades, custo por unidade
3. Nome do arquivo: \`Produtos_DD-MM-AAAA.xls\`

## 📊 Exemplos de Uso

### Exemplo 1: Carne (Rendimento %)
- **Produto**: Picanha
- **Quantidade**: 10 kg
- **Preço/kg**: R$ 45,00
- **Rendimento**: 80%
- **Resultado**:
  - Custo Total: R$ 450,00
  - Custo Líquido: R$ 360,00
  - Perda: R$ 90,00

### Exemplo 2: Bolos (Unidades)
- **Produto**: Bolo de Cenoura
- **Quantidade**: 3 kg
- **Preço/kg**: R$ 12,00
- **Unidades**: 8 bolos
- **Resultado**:
  - Custo Total: R$ 36,00
  - Custo Líquido: R$ 36,00
  - Custo por Unidade: R$ 4,50
  - Perda: R$ 0,00

### Exemplo 3: Sem Rendimento
- **Produto**: Arroz
- **Quantidade**: 5 kg
- **Preço/kg**: R$ 8,00
- **Rendimento**: (deixar vazio)
- **Resultado**:
  - Custo Total: R$ 40,00
  - Custo Líquido: R$ 40,00
  - Perda: R$ 0,00

## 🛠️ Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: Estilização com Tailwind CSS e gradientes
- **JavaScript (ES6+)**: Lógica de negócio e manipulação de dados
- **Canva Data SDK**: Persistência de dados em Planilha Canva
- **Canva Element SDK**: Personalização via interface Canva
- **XML/Excel**: Exportação de dados em formato Excel

## 📦 Estrutura de Dados

\`\`\`javascript
{
  id: "string",                    // ID único do produto
  produto: "string",                // Nome do produto
  quantidade_kg: number,            // Quantidade em kg
  preco_kg: number,                 // Preço por kg em R$
  rendimento_percent: number,       // Percentual de rendimento (0-100)
  unidades_produzidas: number,      // Quantidade de unidades produzidas
  tipo_calculo: "string",           // "percent" ou "units"
  custo_total: number,              // Custo total bruto calculado
  custo_liquido: number,            // Custo líquido calculado
  custo_por_unidade: number,        // Custo individual por unidade
  created_at: "string"              // Data/hora de criação (ISO)
}
\`\`\`

## 🔒 Limitações

- **Máximo de 999 produtos**: Limite técnico da plataforma
- **Dados locais**: Os dados são salvos na sua conta Canva
- **Navegador moderno**: Requer navegador com suporte a ES6+

## 📋 Changelog

### [3.0.0] - 2024-01-15
#### Adicionado
- Dois modos de cálculo: Rendimento (%) e Unidades
- Campo "Unidades Produzidas" para cálculo por quantidade
- Coluna "Custo por Unidade" na tabela
- Badges visuais para identificar tipo de cálculo
- Rendimento agora é opcional
- Exportação Excel com novos campos

#### Melhorado
- Interface com seleção de modo de cálculo
- Flexibilidade para diferentes tipos de produtos
- Cálculos mais precisos para produção em unidades

### [2.0.0] - 2024-01-15
#### Adicionado
- Exportação para Excel
- Botão de download do README
- Logo personalizável
- Créditos do criador

### [1.0.0] - 2024-01-14
#### Adicionado
- Versão inicial da calculadora

## 📄 Licença

MIT License

Copyright (c) 2025 Guilherme Pereira

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## 👤 Autor

**Guilherme Pereira**

- Criador e desenvolvedor principal
- Especialista em gestão de custos alimentícios

## 🤝 Contribuindo

Contribuições, issues e solicitações de recursos são bem-vindas!