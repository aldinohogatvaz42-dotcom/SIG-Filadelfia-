# SIG-Filadelfia-
Um Sistema de Gestão Integrado para uma igreja
SIG-FILADÉLFIA
Sistema de Gestão Integral
Documento do Projecto
FILADÉLFIA — Congregação Malhazine
Versão 1.0 · Novembro de 2026
Este documento descreve o que o sistema deve fazer, como está organizado, o que já existe no protótipo e o que falta construir. O protótipo interactivo acompanha o documento.


Conteúdo
1. Introdução e objectivo
2. A igreja e a sua estrutura
3. Perfis e permissões
4. Módulos do sistema
5. Fluxos principais
6. Base de dados central
7. Segurança e protecção de dados
8. Identidade visual e experiência de uso
9. Estado actual e plano técnico
10. Decisões em aberto
Anexo A — Departamentos
Anexo B — Campos dinâmicos dos documentos


1. Introdução e objectivo
O SIG-FILADÉLFIA é um sistema de gestão integral para a igreja FILADÉLFIA e as suas congregações. O objectivo é centralizar, numa só plataforma, todo o trabalho administrativo e pastoral: membros, famílias, secretaria, liderança, departamentos, ministérios, actividades, planos, finanças, património, comunicação, reuniões, presenças, documentos, relatórios, arquivo e Excel.
Todos os módulos usam uma base de dados central, ligam-se entre si e respeitam as permissões de cada utilizador.
Princípios do sistema
Informação cadastrada uma só vez. Uma pessoa tem uma única ficha, usada por todos os módulos autorizados, sem duplicação.
A igreja define o modelo, o sistema tem os dados. Os documentos são gerados a partir de modelos da própria igreja, com os campos preenchidos automaticamente.
O dinheiro só sai por fluxo autorizado. Nenhum departamento retira dinheiro directamente: há pedido, aprovação, processamento e recibo.
Cada pessoa vê só o que lhe cabe. O acesso depende do perfil, do departamento e da congregação.
Simples de usar. Interface limpa, responsiva e adaptada a telemóvel, tablet e computador, para pessoas com diferentes níveis de conhecimento informático.
2. A igreja e a sua estrutura
A estrutura organizativa registada no sistema é a seguinte.
Nível
Descrição

FILADÉLFIA
Organização.

Congregação Malhazine
Sede.

Zona Central
Zona da sede, com 11 grupos e 4 filiais.

Grupos (11)
Alfa e Omega, Bethel, Caná, Ebenezer, Emanuel, Gólgota, Israel, Jerusalém, Magos do Oriente, Nazaré, Tribo de Judá.

Filiais da Zona Central (4)
Belém, Magoanine 1, Magoanine 2 (Zona 2), Volante 6.

Outras congregações (7)
Boquisso, CMC, Hope City, Mandlakaze, Mateque, Zavala, 1.º de Maio. São independentes de Malhazine, mas prestam contas.


Em todo o sistema, o termo "zona" foi substituído por "grupo", como pedido. Cada grupo e cada filial tem a sua galeria, com os membros e o cadastro.
Congregações independentes
Recomenda-se uma só plataforma, onde cada congregação tem os seus dados e utilizadores. Malhazine vê só o que cada congregação prestar: contas e totais por idade, sexo, estado civil e função eclesiástica. Os dados pessoais dos membros (nomes, contactos) ficam com cada congregação, salvo autorização.
Censo do ramo: a congregação entrega os totais por formulário, ou carrega o modelo Excel com a lista dos seus membros; o sistema calcula os totais e guarda só os números.
Prestação de contas: a congregação submete período, receitas, despesas e contribuição para a sede; a sede aprova ou devolve com motivo. Ao aprovar, a contribuição entra como receita em Finanças.
Entrada faseada: começar por Malhazine e integrar as outras congregações uma a uma; as que ainda não estiverem prontas começam só com a prestação de contas.
3. Perfis e permissões
O sistema usa controlo de acesso por perfil (RBAC). Cada utilizador tem permissões independentes para ver, criar, editar, aprovar, rejeitar, eliminar, exportar, imprimir, gerar documentos e gerar relatórios. Só o Super Administrador configura as permissões e elimina informação importante.
Perfil
Acesso principal

Super Administrador
Tudo, incluindo utilizadores, permissões, backups e eliminações.

Administrador
Tudo, excepto as acções reservadas ao Super Administrador.

Pastor
Direcção: situação geral, aprovações de planos, pedidos de despesa e prestações de contas.

Secretário
Membros, validações, operações, documentos, actas e arquivo.

Tesoureiro/Finanças
Finanças, pagamentos, recibos, orçamento e património.

Líder de Departamento
A sala do seu departamento: convida membros, cria conteúdo e delega permissões.

Líder de Ministério
Ministério, escalas e presenças.

Líder de Zona (grupo)
Membros e presenças do seu grupo.

Líder de Célula/Grupo
Comunicação e presenças.

Líder de Congregação
Entrega o censo e as prestações de contas da sua congregação.

Membro
Painel pessoal, cartão, escalas, avisos, Secretaria Virtual, biblioteca e as salas dos seus departamentos.

4. Módulos do sistema
4.1 Membros, famílias e cartão
Cadastro central: número de registo automático e sequencial (00001, 00002…), nunca repetido; fotografia; nome; sexo; data de nascimento; idade calculada; estado civil; contacto; email; endereço; bairro; localidade; grupo; célula; datas de entrada e de baptismo; função eclesiástica; ministério; departamento; profissão; escolaridade; observações; estado do membro.
Estado civil: solteiro/a, casado/a, viúvo/a, divorciado/a, falecido/a. O cônjuge escolhe-se entre os membros existentes (sem segunda ficha) e a relação JOÃO ↔ MARIA é criada nos dois sentidos. Quando alguém é marcado como falecido, o histórico mantém-se e o cônjuge passa a viúvo/a.
Duplicados: o sistema avisa quando o mesmo nome e data de nascimento já existem.
Famílias e censo: agregados familiares e estatísticas automáticas por sexo, idade, estado civil, grupo, célula, departamento, ministério, função, profissão e escolaridade.
Cartão do membro: digital e para impressão, com logotipo, nome da igreja, fotografia, nome, número, idade, função, grupo e código QR. O QR abre só os dados autorizados (nome, número, função, grupo e estado). Pode visualizar, gerar PDF, baixar e imprimir.
4.2 Secretaria Virtual
A Secretaria é virtual e aberta a todos: qualquer membro vê anúncios, usa a biblioteca e faz pedidos.
Pedidos: declaração de membro, de baptismo e de casamento, transferência, alteração de dados, cartão de membro (incluindo 2.ª via em caso de perda), certificado e outros.
Pagamento antes do pedido: as taxas são definidas pelo administrador. O membro paga por M-Pesa, e-Mola, e-Kesh, cartão bancário ou referência bancária. Só depois de autorizado pela Secretaria pode baixar o documento.
Validações: alterações a dados oficiais (nome, nascimento, estado civil, grupo, departamento, função) só entram em vigor depois de validadas pela Secretaria, com motivo obrigatório em caso de rejeição.
Operações: cadastro, actualização, transferência, mudança de grupo e mudança de departamento, todas auditadas.
Biblioteca: a igreja carrega vários livros de uma vez; todos podem abrir e baixar.
4.3 Departamentos como salas
Cada departamento é um órgão com a sua própria sala, onde decorre o seu trabalho. O líder convida pessoas já registadas na igreja, e a pessoa só entra depois de aceitar o convite. Uma pessoa pode pertencer a vários departamentos.
Na sala: anúncios, mensagens (todos os membros da sala podem escrever), reuniões (com presenças, acta e link de vídeo opcional), actividades, plano, membros e escalas.
Líder e delegados: só o líder cria conteúdo, ou dá permissão a um membro, escolhendo o quê: anúncios, reuniões, actividades, plano, repertório ou escalas. O líder vê dos membros só a função e o contacto.
Louvor e Adoração: além do comum, tem repertório (música, autor, tom, andamento, ficheiro de cifra ou letra, notas) e equipas (vocalistas principais, coristas, instrumentistas com o instrumento, dirigentes e técnicos). As escalas do culto incluem as músicas.
Cada membro sabe a sua actividade: o painel pessoal junta as actividades, reuniões e escalas de todos os departamentos a que pertence.
Independência com limites: o plano e o orçamento continuam a ser aprovados pela direcção, e o dinheiro só sai por pedido de despesa.
4.4 Ministérios, escalas e presenças
Ministérios: louvor, coral, instrumentistas, jovens, crianças, evangelismo, intercessão, missões, ensino e outros, cada um com líder, membros, actividades, escalas e relatórios.
Escalas: pregadores, dirigentes, músicos, cantores, técnicos de som, mídia, recepção, diáconos e intercessores; o responsável é notificado e confirma.
Presenças: cultos, Escola Bíblica, reuniões, ensaios, eventos, células, departamentos e ministérios; registo manual ou por QR/cartão; estatísticas por tipo, evento e membro e lista de faltosos.
4.5 Planos, actividades e relatórios
Planos: anual, trimestral ou mensal, com objectivos, responsáveis, datas, local, orçamento, recursos e resultados esperados. Estados: rascunho, submetido, em análise, aprovado, rejeitado (com motivo), em execução, concluído e cancelado.
Actividades: nome, departamento, ministério, responsável, data, hora, local, descrição, participantes previstos, orçamento, recursos e estado. No fim, o departamento apresenta o relatório.
4.6 Finanças
Entradas, saídas e saldo são separados. As receitas têm categorias (dízimos, ofertas, doações, contribuições e outras), e as despesas também (compras, pagamentos, transferências e outras).
Pedido de despesa: departamento → pedido → Pastor aprova → Finanças processa (método e referência) → recibo → despesa lançada → saldo actualizado. Exemplo: saldo de 5.000 MT, pedido de 2.000 MT, saldo final de 3.000 MT.
Orçamento anual: cada departamento apresenta o valor solicitado; a direcção aprova; o sistema mostra solicitado × aprovado × gasto × saldo.
Recibos: automáticos, com número, data, beneficiário, valor, motivo, departamento, responsável, método, referência, autorização e QR; visualizar, baixar Excel e PDF, imprimir e arquivar.
Pagamentos móveis e bancários: o servidor envia o pedido de pagamento à operadora; o cliente confirma com o PIN; a operadora avisa o servidor (callback); o sistema reconcilia sozinho e regista a receita.
4.7 Documentos, modelos e arquivo
Gestor de modelos: a igreja cria, edita, carrega, duplica, activa e desactiva modelos, cria novas versões e define campos automáticos. O sistema nunca obriga a usar documentos pré-definidos.
Tipos de modelo: declarações, certificados, cartas, transferências, apresentações, autorizações, convocatórias, actas, documentos financeiros e relatórios (com cabeçalho, introdução, desenvolvimento, resultados, dificuldades, conclusão, recomendações, assinaturas e rodapé).
Automação: modelo + dados + automação = documento final. O sistema pergunta o período, identifica o departamento, procura actividades, participantes, despesas, orçamento e presenças, calcula as estatísticas e preenche o modelo.
Documentos financeiros: os valores vêm do módulo financeiro, ficam bloqueados e levam um selo de integridade; ao abrir do arquivo, o sistema avisa se o documento foi alterado.
Formatos e botões: visualizar, editar antes de gerar, baixar Excel, baixar PDF, imprimir, partilhar e guardar no arquivo. Impressão em A4, retrato ou paisagem, com margens, cabeçalho, rodapé e número de páginas, depois de uma pré-visualização.
Arquivo e versões: cada documento guarda número, tipo, data, autor, departamento, período, modelo, versão e estado, e pesquisa-se por qualquer um deles ou por palavra-chave. Os documentos antigos nunca mudam quando o modelo muda.
Excel oficial: a igreja fornece o seu modelo Excel; o sistema preenche-o mantendo a estrutura e as fórmulas. Exportação completa para .xlsx com 20 folhas (membros, famílias, crianças, liderança, departamentos, ministérios, grupos, células, baptismos, casamentos, actividades, planos, finanças, entradas, despesas, orçamento, recibos, património, relatórios e estatísticas).
Exportação em massa: seleccionar vários membros e gerar documentos, exportar Excel, gerar PDFs, imprimir e arquivar.
4.8 Comunicação e reuniões
Comunicação: avisos e comunicados com comentários, mural comum e conversas por grupo (igreja, grupo, departamento, ministério, célula e família), respeitando permissões.
Reuniões: nome, data, hora, local, participantes, agenda e documentos; depois, presenças, acta, decisões, tarefas, responsáveis e prazos.
4.9 Património
Instrumentos, computadores, câmaras, microfones, mesas, cadeiras, veículos, edifícios e equipamentos, com código, categoria, data de aquisição, valor, estado, localização, responsável, fotografia, manutenção e histórico. Inclui inventário por categoria e conferência física.
4.10 Painéis, notificações e pesquisa
Painéis: administrativo (indicadores, aniversariantes, próximos eventos, alertas e fluxo geral), do Pastor (aprovações pendentes), financeiro e do membro.
Notificações: novo cadastro, alteração solicitada, plano submetido, aprovado ou rejeitado, pedido financeiro e sua aprovação, pagamento, recibo, reunião, actividade, escala, documento e aniversário.
Pesquisa global: membros, famílias, departamentos, ministérios, actividades, documentos, recibos, transacções e património, respeitando as permissões.
4.11 Relatórios automáticos
Relatório geral da igreja, de membros, familiar, de grupos, de células, de departamentos, de ministérios, de actividades, financeiro, de despesas, de orçamento, de assiduidade, de crescimento e anual. Todos usam os modelos definidos pela igreja.
5. Fluxos principais
Fluxo
Passos

Cadastro de membro
Membro → cadastro → Secretaria → validação → base de dados central → família, grupo, célula, ministério e departamento.

Despesa
Departamento → pedido de despesa → Pastor aprova → Finanças processa → recibo → despesa lançada → saldo actualizado.

Plano
Departamento → submeter → direcção analisa → aprovar ou rejeitar (motivo) → execução → relatório.

Pedido à Secretaria
Membro → pedido → pagamento → Secretaria autoriza → documento gerado do modelo → o membro baixa.

Alteração de dados oficiais
Membro → pedido → Secretaria valida ou rejeita → dado actualizado e auditado.

Departamento
Líder → convite → membro aceita → entra na sala → actividades, escalas e mensagens.

Congregação independente
Congregação → censo e prestação de contas → sede aprova ou devolve → contribuição lançada em Finanças.

Documento
Modelo + dados + automação → documento → Excel/PDF → download → impressão → arquivo.

6. Base de dados central
Todos os módulos usam a mesma base de dados, com chaves primárias, chaves estrangeiras, índices e integridade referencial. A cadeia de relações é: membros → famílias → grupos → células → departamentos → ministérios → actividades → planos → finanças → documentos → relatórios.
Tabela
Chave primária
Chaves estrangeiras
Índices

membros
id
grupo, célula, departamento, cônjuge
registo (único), nome + nascimento

familias
id
responsável → membros
grupo

grupos
id
líder → membros
nome (único)

celulas
id
grupo
nome

departamentos
id
líder → membros
nome (único)

ministerios
id
líder → membros
nome

actividades
id
departamento, ministério, plano
data

planos
id
departamento
estado

pedidos_despesa
id
departamento
estado

transaccoes
id
pedido, departamento, categoria
data, tipo

recibos
id
transacção
número (único)

documentos
id
modelo, departamento, autor
número (único), tipo

modelos
id
—
nome + versão (único)

presencas
id
evento, membro
(evento, membro) único

auditoria
id
utilizador
data


Todas as tabelas ligam-se também a uma congregação, para isolar os dados de cada uma. Backups diários, semanais e mensais, com recuperação reservada ao Super Administrador.
7. Segurança e protecção de dados
Controlo
No protótipo
No sistema real

Palavras-passe
Hash SHA-256 com sal, no navegador
Argon2id ou bcrypt no servidor

Sessões
Lista de sessões, terminar sessão, bloqueio após 5 tentativas
Cookies HttpOnly/Secure, expiração e renovação

RBAC
Perfis, módulos e acções por perfil
Verificado em cada pedido à API

Auditoria
Acção, data, registo, valor anterior e novo
Tabela imutável, com IP e dispositivo

Validação
Campos obrigatórios e duplicados
Revalidação no servidor

SQL Injection
Não se aplica
Consultas parametrizadas ou ORM

XSS
Todo o texto é escapado antes de aparecer
Mais Content-Security-Policy

Backups
Manual, diário, semanal e mensal (simulados)
Automáticos, cifrados e fora do servidor

Dados pessoais
QR com dados mínimos; congregações enviam só totais
Cifra em repouso e acesso por congregação

Controlo de acesso
Menu e acções por perfil
Isolamento por congregação

8. Identidade visual e experiência de uso
Nome: SIG-FILADÉLFIA, Sistema de Gestão Integral. O administrador altera nome, lema, endereço, contactos e cores sem mexer no código.
Cores: laranja e branco; aplicação toda branca.
Papéis de parede: seis desenhos em laranja que mudam sozinhos no ecrã de entrada e no painel inicial, com opção de os usar em toda a aplicação. O administrador também pode carregar o seu papel de parede, o logotipo e a fotografia de perfil.
Flyers: cada departamento gera um flyer com o seu nome, editável (título, data, hora, local, descrição e cor), que se baixa como imagem.
Dispositivos: interface responsiva para Android, tablet e computador.
9. Estado actual e plano técnico
Existe um protótipo interactivo que mostra como o sistema funciona. Os dados ficam só na memória do navegador e perdem-se ao recarregar a página. Para o sistema real faltam o servidor, a base de dados e a API.
Componente
Protótipo
Sistema real

Frontend
Completo
Construir a partir do protótipo

Backend e API
Não existe
A construir (REST)

Base de dados
Esquema desenhado (15 tabelas)
PostgreSQL

Autenticação
Simulada: login, conta, recuperação, sessões
No servidor

Permissões
Simuladas
No servidor

Finanças e aprovações
Fluxo completo em memória
No servidor

Pagamentos
Simulados
Integração com operadoras e banco, por agregador autorizado

Excel, PDF e impressão
No navegador
Também no servidor, preservando o modelo oficial

Backup
Simulado
Automático e cifrado


Arquitectura sugerida
Aplicação web responsiva (PWA), API REST e base de dados PostgreSQL, com armazenamento de ficheiros.
Back-end em Node.js (NestJS) ou Laravel, com sessões seguras e RBAC verificado em cada pedido.
Multi-congregação: todas as tabelas com identificador da congregação e isolamento por linha.
Pagamentos por M-Pesa, e-Mola, e-Kesh e banco, com confirmação por callback e reconciliação automática. As credenciais ficam só no servidor; a igreja precisa de existência legal e de passar os testes de cada operadora.
Documentos: motor de modelos com campos {{CAMPO}} e exportação PDF e Excel no servidor.
Fases de entrega
Fase
Conteúdo

1
Membros, grupos, Secretaria Virtual e documentos.

2
Finanças, orçamento e pagamentos.

3
Departamentos (salas), ministérios, escalas, presenças e comunicação.

4
Congregações independentes: censo do ramo e prestação de contas.

10. Decisões em aberto
Confirmar a grafia dos nomes: "Magos do Oriente" (foi escrito "Magoa do Oriente") e "Alfa e Omega".
Indicar os nomes reais das células (hoje: Célula 1 a 4, provisórias).
Definir os valores reais das taxas (os do protótipo, de 100 a 250 MT, são exemplos).
Decidir se a sede quer das congregações só totais ou também uma lista nominal, e o que mais devem entregar além das contas.
Indicar o endereço completo da sede, o lema da igreja e o logotipo.
Iniciar os contactos com as operadoras e o banco para os pagamentos reais.
Decidir se cada congregação independente tem tesouraria e líderes próprios, ou depende de Malhazine.
Anexo A — Departamentos
Secretaria; Finanças/Tesouraria; Evangelismo; Missões; Escola Bíblica; Jovens; Crianças; Senhoras; Homens; Louvor e Adoração; Mídia e Comunicação; Intercessão; Acção Social; Família e Casamento; Diaconato; Património e Logística; Educação e Formação; Tecnologia e Sistemas; Protocolo; Recepção e Acolhimento; Conselho/Liderança. O administrador pode acrescentar, editar, desactivar ou reactivar departamentos.
Anexo B — Campos dinâmicos dos documentos
Nos modelos escreve-se {{NOME_DO_CAMPO}} e o sistema substitui pelos dados.
Campo
Significado

{{NOME_IGREJA}}, {{LOGOTIPO}}, {{ENDERECO}}
Identidade da igreja.

{{NOME_DEPARTAMENTO}}, {{RESPONSAVEL}}
Departamento e responsável.

{{DATA
