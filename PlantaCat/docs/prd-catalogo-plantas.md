# PRD – PlantaCat: Sistema de Cadastro e Catálogo Online de Plantas

**Versão:** 1.0  
**Data:** Junho de 2026  
**Status:** Rascunho  

---

## 1. Visão Geral do Produto

### 1.1 Resumo

O **PlantaCat** é uma plataforma web para cadastro, catalogação e divulgação de informações sobre plantas ornamentais, medicinais e exóticas. O sistema permite que entusiastas, botânicos amadores, floriculturas e educadores registrem fichas completas de plantas — com dados técnicos, cuidados, curiosidades e informações culturais — e as publiquem em um catálogo público acessível pela internet.

### 1.2 Problema que resolve

Hoje, informações sobre plantas estão dispersas em blogs, fóruns, vídeos e livros físicos, muitas vezes desatualizadas, sem padrão ou credibilidade. Não existe uma plataforma centralizada, em português, que combine:

- Dados botânicos confiáveis
- Guias práticos de cuidados
- Curiosidades e informações culturais / espirituais
- Contribuição colaborativa da comunidade
- Catálogo público de fácil consulta

### 1.3 Proposta de valor

> *"Um lugar onde qualquer pessoa pode encontrar tudo sobre uma planta — do científico ao folclórico — e onde apaixonados por plantas constroem juntos o maior catálogo em português."*

---

## 2. Objetivos e Métricas de Sucesso

| Objetivo | Métrica | Meta (6 meses) |
|---|---|---|
| Crescimento do catálogo | Número de plantas cadastradas | 500 fichas |
| Engajamento da comunidade | Usuários cadastrados e ativos | 1.000 usuários |
| Alcance público | Acessos mensais ao catálogo público | 10.000 visitas/mês |
| Qualidade do conteúdo | Taxa de fichas com dados completos (≥ 80% dos campos) | 70% das fichas |
| Retenção | Usuários que retornam para cadastrar mais de uma planta | 40% |

---

## 3. Personas

### 3.1 Maria, 38 anos — Entusiasta de plantas de interior
- Tem mais de 30 vasos em casa, incluindo suculentas e fitônias
- Quer registrar sua coleção e compartilhar com amigas
- Não tem formação técnica em botânica
- Usa smartphone principalmente, acessa pelo celular
- **Necessidade:** interface simples, campos claros, poder adicionar fotos

### 3.2 Pedro, 52 anos — Dono de floricultura
- Vende plantas ornamentais há 15 anos
- Quer divulgar seu catálogo de espécies disponíveis com informações de cuidado para os clientes
- Acessa pelo computador no balcão da loja
- **Necessidade:** cadastro em massa, página pública da loja, ficha com informações de compra

### 3.3 Carla, 26 anos — Estudante de biologia
- Faz pesquisa sobre espécies nativas do cerrado
- Quer contribuir com dados científicos precisos
- Usa desktop, valoriza rigor nos campos e referências
- **Necessidade:** campos técnicos (família, gênero, espécie, habitat), exportação de dados

### 3.4 Visitante anônimo
- Chegou via busca no Google procurando "como cuidar de fitônia"
- Não quer se cadastrar, só quer a informação
- **Necessidade:** catálogo público sem login, busca rápida, layout limpo

---

## 4. Funcionalidades do Sistema

### 4.1 Módulo de Autenticação

- Cadastro com nome, e-mail e senha
- Login por e-mail/senha
- Login social (Google) — fase 2
- Recuperação de senha por e-mail
- Perfil de usuário com nome, foto, bio e tipo de conta (entusiasta, profissional, pesquisador)

### 4.2 Módulo de Cadastro de Plantas (área restrita)

Formulário de ficha completa com as seguintes seções:

#### Identificação
- Nome popular (campo livre, múltiplos nomes separados por vírgula)
- Nome científico (gênero + espécie)
- Família botânica
- Outros nomes conhecidos
- Foto principal (upload de imagem)
- Galeria de fotos (até 10 imagens)

#### Informações Básicas
- Descrição geral da planta (texto longo)
- Tipo: ornamental / medicinal / comestível / exótica / nativa / outra
- Porte: mini / pequeno / médio / grande / árvore
- Ciclo de vida: anual / bienal / perene
- É tóxica para humanos? (sim / não / parcialmente)
- É tóxica para animais? (sim / não / parcialmente)

#### Origem e Distribuição
- País(es) de origem
- Bioma / habitat natural (floresta tropical, semiárido, cerrado, etc.)
- Regiões onde ocorre naturalmente
- Data / período da descrição botânica formal
- Quem descreveu / descobriu (botânico responsável)

#### Guia de Cuidados
- Necessidade de luz (pleno sol / meia sombra / sombra / luz indireta)
- Frequência de rega (diária / semanal / quinzenal / mensal)
- Umidade do ar necessária (baixa / média / alta)
- Temperatura ideal (faixa em °C)
- Tipo de solo ideal
- Necessidade de adubação (frequência e tipo)
- Dicas de poda
- Como reproduzir (semente / estaca / divisão de touceira / folha)
- Dificuldade de cultivo (fácil / intermediário / difícil)

#### Curiosidades
- Campo de texto livre para fatos interessantes, recordes, usos históricos

#### Informações Culturais e Populares *(seção diferencial do produto)*
- Significado simbólico
- Uso no Feng Shui
- Mitos e crenças populares
- Ditados ou expressões relacionadas
- Usos medicinais populares (com aviso de que não substituem orientação médica)
- Referências culturais (literatura, arte, religião)

#### Metadados
- Tags / palavras-chave
- Status da ficha: rascunho / publicado / em revisão
- Nível de completude (calculado automaticamente pelo sistema)

### 4.3 Módulo de Catálogo Público

- Página inicial com destaque para plantas recém-adicionadas e mais acessadas
- Busca por nome popular, científico ou tag
- Filtros: tipo de planta, dificuldade de cultivo, nível de luz, toxicidade
- Card de listagem com foto, nome popular, nome científico e dificuldade
- Página de detalhe da planta com todas as informações da ficha
- Compartilhamento via link, WhatsApp e redes sociais
- SEO otimizado: URL amigável (ex: `/plantas/fitonia-folha-fina`)

### 4.4 Módulo de Gestão (painel do usuário)

- Lista de plantas cadastradas pelo usuário
- Indicador de completude de cada ficha
- Editar / excluir fichas
- Visualizar quantas vezes cada planta foi vista no catálogo público
- Favoritar plantas de outros usuários

### 4.5 Módulo de Moderação *(fase 2)*

- Fila de fichas aguardando revisão
- Aprovação / rejeição com comentário
- Usuários com perfil "pesquisador verificado" têm publicação direta
- Denúncia de conteúdo incorreto pela comunidade

---

## 5. Requisitos Não Funcionais

| Requisito | Detalhe |
|---|---|
| Responsividade | Funciona em mobile, tablet e desktop |
| Acessibilidade | Contraste mínimo WCAG AA, textos alternativos em imagens |
| Performance | Catálogo público carrega em menos de 3 segundos |
| SEO | Páginas de plantas indexáveis por buscadores |
| Idioma | Português brasileiro como padrão; inglês como fase 2 |
| Segurança | Senhas com hash (bcrypt), proteção CSRF, sanitização de inputs |
| Escalabilidade | Suporta até 50.000 fichas sem degradação de performance |

---

## 6. Jornadas Principais do Usuário

### Jornada 1 — Cadastrar uma nova planta
1. Usuário faz login
2. Clica em "Cadastrar Nova Planta"
3. Preenche os campos por seções (pode salvar como rascunho a qualquer momento)
4. Faz upload de fotos
5. Publica a ficha
6. Recebe URL pública para compartilhar

### Jornada 2 — Visitante encontra uma planta
1. Visitante busca no Google "como cuidar de fitônia"
2. Encontra a página da fitônia no PlantaCat
3. Lê todas as informações: cuidados, curiosidades, crenças populares
4. Compartilha o link no WhatsApp com um amigo
5. (Opcional) Se cadastra para adicionar sua própria planta

### Jornada 3 — Floricultura divulga seu catálogo
1. Pedro cria conta como "Perfil Profissional"
2. Cadastra as 20 espécies que vende
3. Compartilha o link do seu perfil público com clientes
4. Clientes acessam e veem as fichas completas com cuidados

---

## 7. Estrutura de Dados — Entidade Planta

```
Planta {
  id
  nome_popular[]
  nome_cientifico
  familia_botanica
  outros_nomes[]
  foto_principal (URL)
  galeria[] (URLs)
  descricao_geral
  tipo[]
  porte
  ciclo_vida
  toxica_humanos
  toxica_animais
  pais_origem[]
  habitat
  regioes[]
  data_descricao_botanica
  descoberto_por
  necessidade_luz
  frequencia_rega
  umidade_ar
  temperatura_min
  temperatura_max
  tipo_solo
  adubacao
  dicas_poda
  formas_reproducao[]
  dificuldade_cultivo
  curiosidades
  simbolismo
  feng_shui
  mitos_crencas
  usos_medicinais_populares
  referencias_culturais
  tags[]
  status (rascunho | publicado | em_revisao)
  completude (0-100%)
  criado_por (user_id)
  criado_em
  atualizado_em
  visualizacoes
}
```

---

## 8. Fases de Entrega

### Fase 1 — MVP (2 meses)
- [ ] Autenticação (cadastro e login)
- [ ] Formulário de cadastro de planta com campos essenciais
- [ ] Catálogo público com busca e filtros básicos
- [ ] Página de detalhe da planta
- [ ] Painel do usuário (minhas plantas)
- [ ] Upload de fotos
- [ ] Responsivo mobile

### Fase 2 — Comunidade (mês 3-4)
- [ ] Moderação de conteúdo
- [ ] Sistema de favoritos
- [ ] Perfis públicos de usuários
- [ ] Login social (Google)
- [ ] Compartilhamento social otimizado (Open Graph)
- [ ] SEO avançado (sitemap, schema markup para plantas)

### Fase 3 — Crescimento (mês 5-6)
- [ ] API pública de consulta
- [ ] Exportação de fichas em PDF
- [ ] Perfis profissionais (floriculturas)
- [ ] Newsletter de plantas da semana
- [ ] Versão em inglês

---

## 9. Fora do Escopo (por enquanto)

- Loja/e-commerce de plantas
- Identificação de plantas por foto (IA)
- App nativo iOS/Android
- Sistema de agendamento de cuidados / lembretes de rega
- Fórum ou sistema de comentários nas fichas

---

## 10. Riscos e Mitigações

| Risco | Probabilidade | Impacto | Mitigação |
|---|---|---|---|
| Fichas com informações incorretas | Alta | Alto | Moderação antes de publicar; denúncia pela comunidade |
| Baixo volume de cadastros iniciais | Média | Alto | Pré-popular com 50 plantas pelo time antes do lançamento |
| Imagens com direitos autorais | Média | Médio | Exigir que o usuário confirme que possui os direitos da foto |
| Conteúdo de uso medicinal inadequado | Média | Alto | Aviso legal obrigatório em todas as fichas com uso medicinal |
| Baixo SEO inicial | Alta | Médio | Investir em metadados ricos e URLs semânticas desde o início |

---

## 11. Referências e Inspirações

- [Wikipedia - Succulent plant](https://en.wikipedia.org/wiki/Succulent_plant)
- [Gardeners World - Fittonia Care](https://www.gardenersworld.com/how-to/grow-plants/grow-care-fittonia/)
- [Plants & Flowers Foundation Holland](https://www.plantsandflowersfoundationholland.org/en/indoor-plantguide/fittonia/)
- [Missouri Botanical Garden](https://www.missouribotanicalgarden.org)
- Conteúdo produzido nas sessões de pesquisa sobre Suculentas e Fitônia (PlantaCat, Junho/2026)
