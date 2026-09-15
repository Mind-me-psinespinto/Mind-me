# Publicar o site Mind.me

Repositório: https://github.com/inspnt/Mind-me
Domínio: **mind-me-psinespinto.pt**

## Ficheiros a carregar
Tudo o que está dentro da pasta `site/` (os ficheiros, não a pasta):

```
index.html          página única — informação e marcação de consultas
marcacao.html       reencaminha para a secção de marcação (mantém links antigos a funcionar)
privacidade.html    política de privacidade
og.png              imagem que aparece ao partilhar o link
favicon.png         ícone do separador do navegador
logo-art.png        logótipo usado na imagem de partilha
retrato.jpg         fotografia
sitemap.xml         mapa do site para os motores de busca
robots.txt          autoriza a indexação
CNAME               indica o domínio ao GitHub Pages
.nojekyll           ficheiro vazio, evita processamento indevido
```

O site não usa cookies nem ferramentas de medição de visitas.

---

## 0. Envio automático do formulário · já feito

A chave do Web3Forms já está colada no `index.html`. Os pedidos de marcação chegam sozinhos a `psinespinto.mind.me@hotmail.com`, com o assunto `Pedido de marcação · [nome]` e o email da pessoa como remetente — responder é só clicar em Responder.

Nada mais a fazer neste ponto. Se um dia quiser mudar o email de destino, altera-se na conta do Web3Forms, não no site.

**Porque é preciso este serviço.** Uma página aberta no navegador de outra pessoa não pode enviar email em seu nome — se pudesse, qualquer site do mundo enviaria mensagens a fingir ser você. O Web3Forms faz essa entrega e é invisível para quem visita: a pessoa nunca sai da página nem vê outro nome.

---

---

## 1. Registar o domínio · 5 min
Registar `mind-me-psinespinto.pt` num registador `.pt` (Amen, PTisp, Dominios.pt ou a .PT). Entre 15 e 25 € por ano. Recusar os extras propostos na compra — alojamento, email e construtor de sites não são necessários.

## 2. Carregar os ficheiros · 5 min

No repositório `inspnt/Mind-me`:

1. **Add file → Upload files**
2. Arrastar os ficheiros da pasta `site/`
3. **Commit changes**

O `.nojekyll` começa por ponto e o computador tende a escondê-lo. Se não aparecer, criar com **Add file → Create new file**, nome `.nojekyll`, conteúdo vazio.

## 3. Ligar o GitHub Pages · 2 min

**Settings → Pages**

- Source: `Deploy from a branch`
- Branch: `main`, pasta `/ (root)` → **Save**
- Custom domain: `mind-me-psinespinto.pt` → **Save**
- **Enforce HTTPS**: marcar só depois de o endereço abrir (passo 4)

## 4. Apontar o DNS · 5 min + espera

No painel do registador, na zona DNS:

| Tipo | Nome | Valor |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | inspnt.github.io |

Propagação: 15 minutos a 24 horas. Até lá o endereço pode não abrir — é esperado.

## 5. Google Search Console · 10 min

1. search.google.com/search-console → **Adicionar propriedade** → *Prefixo do URL* → `https://mind-me-psinespinto.pt`
2. Verificar pelo **registo DNS TXT** indicado, na mesma zona DNS do passo 4
3. **Sitemaps** → escrever `sitemap.xml` → **Enviar**
4. **Inspeção de URL** → colar `https://mind-me-psinespinto.pt/` → **Pedir indexação**

Indexação: 2 dias a 2 semanas. Confirmar depois com a pesquisa `site:mind-me-psinespinto.pt`.

## 6. Google Business Profile · 15 min

É esta ficha, mais do que o site, que faz aparecer nas pesquisas locais do tipo "psicólogo Santa Maria da Feira". Criar em business.google.com.

- Nome: `Mind.me · Inês Pinto — Psicóloga`
- Categoria principal: `Psicólogo`; secundárias: `Psicoterapeuta`, `Serviço de saúde mental`
- Website: `https://mind-me-psinespinto.pt`
- Botão de marcação: `https://mind-me-psinespinto.pt/#marcar`
- Telefone: não indicado, por opção
- Moradas:
  - Edifício Quinta, Rua do Cedro 302, 4535-198 Mozelos, Santa Maria da Feira
  - Rua 14, n.º 437, Espinho
- Horários (todos mediante marcação prévia):
  - Mozelos: Segunda-feira, Terça-feira, Quarta-feira e Sexta-feira, 16:00–18:30
  - Espinho: Quarta-feira e Quinta-feira, 15:00–18:30
- Atributos: `Consultas online`, `Atendimento com marcação`

**Descrição (colar tal e qual)**

> Acompanhamento psicológico para crianças, jovens, adultos e famílias, em Santa Maria da Feira, em Espinho e à distância. Inês Pinto é psicóloga inscrita na Ordem dos Psicólogos Portugueses (n.º 44445) e formadora certificada, com prática assente em evidência científica e supervisão clínica especializada. Áreas de intervenção: ansiedade, gestão do stress e regulação emocional; avaliação e intervenção infantojuvenil; parentalidade e dinâmica familiar; comportamentos aditivos, incluindo uso problemático de ecrãs; competências socioemocionais e literacia em saúde mental. Também desenha e dinamiza formação para escolas, instituições e equipas. Marcação por email ou pelo formulário do site.

**Duas cautelas antes de submeter**

- Falar primeiro com as clínicas. O Google não aceita duas fichas na mesma morada para a mesma categoria: se a Cuidar para Crescer ou a Reflexus K já tiverem ficha, a sua é recusada ou suspensa. A alternativa é ser acrescentada como profissional na ficha delas.
- A ficha está sujeita ao regime da publicidade em saúde: sem promessas de resultado, sem preços comparativos, sem testemunhos de utentes. O texto acima já respeita isso.

---

## Confirmar que correu bem

1. `inspnt.github.io/Mind-me` abre o site — poucos minutos após o upload
2. `mind-me-psinespinto.pt` abre o site — 15 min a 24 h
3. Aparece o cadeado na barra do navegador — até 1 h depois; só então marcar **Enforce HTTPS**

## Alterar o site depois

Os textos vivem dentro do `index.html`. Peça-me no chat a alteração que quiser, eu devolvo o ficheiro corrigido e basta voltar a carregá-lo no GitHub (**Add file → Upload files**, substitui o anterior).
