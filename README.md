# Controle Financeiro — Painel

Painel de indicadores financeiros (faturamento, rentabilidade, despesas, backlog, cotações e câmbio) gerado a partir da planilha `CONTROLE_FINANCEIRO.xlsx`.

É um site 100% estático: um único arquivo `index.html`, sem servidor e sem banco de dados. Os gráficos usam Chart.js e a leitura de planilhas usa SheetJS, ambos carregados via CDN.

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (por exemplo, `controle-financeiro`).
2. Envie o arquivo `index.html` (e este `README.md`) para o repositório — pode arrastar os arquivos direto na página do repositório em **Add file → Upload files**.
3. No repositório, vá em **Settings → Pages**.
4. Em **Source**, escolha **Deploy from a branch**, selecione a branch `main` e a pasta `/ (root)`, e clique em **Save**.
5. Em 1–2 minutos o site fica disponível em `https://SEU-USUARIO.github.io/controle-financeiro/`.

## Como atualizar os dados

Você tem duas opções:

- **Sem mexer em código:** abra o site publicado e arraste a versão nova da planilha `CONTROLE_FINANCEIRO.xlsx` na área indicada no fim da página. O painel é atualizado na hora, **somente no seu navegador** (nada é enviado a servidor algum — ao recarregar a página, voltam os dados embutidos).
- **Atualização permanente:** edite o bloco `DATA` no início do `<script>` dentro do `index.html` (datas e valores) e envie o arquivo atualizado para o repositório.

## Estrutura esperada da planilha

O leitor procura, na primeira aba, uma linha de cabeçalho começando com `ITENS DO I-LOG` seguida de colunas com datas, e abaixo dela as linhas de indicadores com valores numéricos — exatamente o formato da sua planilha atual.

## Observação sobre privacidade

Ao publicar em um repositório **público**, os números ficam visíveis para qualquer pessoa na internet. Se os dados forem sensíveis, crie o repositório como **privado** — nesse caso o GitHub Pages exige plano pago para páginas privadas — ou avalie outra hospedagem com senha.
