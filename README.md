# Gerador de Proposta de Compra — Premier Garden

Ferramenta web gratuita para preencher, assinar e gerar a **Proposta de Compra do Premier Garden** (Realiza Empreendimento Rio Verde IV SPE Ltda.) em Word (.docx) ou PDF.

Ela roda inteira no navegador, em um único arquivo HTML. Não há servidor, cadastro nem instalação.

## Como usar

**Online (GitHub Pages)**
1. Ative o GitHub Pages em *Settings → Pages → Branch: `main` / root*.
2. Acesse `https://<seu-usuario>.github.io/<nome-do-repositorio>/`.

**Offline**
1. Baixe o `index.html`.
2. Abra-o no Chrome, Edge ou Firefox.

**Fluxo**
1. Preencha os dados no painel à esquerda. O documento à direita atualiza em tempo real.
2. (Opcional) Envie as fotos das assinaturas em **Assinaturas (fotos)**.
3. Clique em **Gerar Word (.docx)** ou **Imprimir / PDF**.

## Funcionalidades

| Recurso | Descrição |
|---|---|
| Pré-visualização ao vivo | Layout fiel ao formulário oficial, em 4 páginas A4 |
| Painel de conferência | Soma da forma de pagamento × preço, Parte I + II × comissão, parcelas × total, CPF/CNPJ válidos, campos pendentes |
| Máscaras | CPF, CNPJ, CEP, telefone, datas e valores em R$ |
| Cálculo de parcela | Botão **÷** divide o total pelo nº de prestações |
| Assinaturas por foto | Remove o fundo automaticamente (corrige sombra e iluminação desigual); permite girar e escolher a cor da tinta |
| Posicionamento da assinatura | Arraste no documento; redimensione pela alça, pela roda do mouse ou com os botões −/+; ajuste fino pelas setas do teclado |
| Cores | Cor dos dados preenchidos e cor dos textos do formulário |
| Exportação | Word (.docx) editável e impressão/PDF |
| Rascunhos | Salvamento automático no navegador; **Exportar/Importar dados** em .json |
| Nova proposta | Limpa os dados do cliente e mantém os do corretor |

## Privacidade

- Nenhum dado é enviado para servidores. Tudo é processado localmente no navegador.
- O rascunho fica no `localStorage` do próprio navegador. Em computador compartilhado, use **Nova proposta** ao terminar.
- Não publique arquivos `.json` exportados: eles contêm dados pessoais (CPF, renda, assinaturas).

## Dependências (carregadas por CDN)

- [docx](https://github.com/dolanmiu/docx) 9.7.1: geração do arquivo Word. Exige internet só para o botão **Gerar Word**; **Imprimir / PDF** funciona offline.
- [Lucide](https://lucide.dev): ícones (opcional; sem internet os botões continuam funcionando).
- Fonte Inter (Google Fonts).

## Estrutura

```
index.html                                        # gerador completo (arquivo único)
modelo/Proposta_de_Compra_Premier_Garden_em_branco.docx   # formulário em branco para Word
assets/logo-premier-garden.png                    # logo com fundo transparente
```

## Avisos

- A assinatura inserida como imagem formaliza a proposta, mas **não substitui assinatura eletrônica certificada** (gov.br / ICP-Brasil). Insira apenas assinaturas enviadas e autorizadas pelo próprio signatário.
- A marca e o logotipo *Premier Garden* pertencem aos seus titulares. Esta ferramenta não é um canal oficial da incorporadora, e a proposta só é oficializada após confirmação da vendedora.
- Os textos do formulário seguem o modelo oficial, com correções de português.
