Etapa 4: Autenticação Centralizada (OpenLDAP)
1. Comandos de Instalação e Configuração
O serviço de diretórios OpenLDAP foi configurado sob o sufixo de domínio corporativo dc=technet,dc=local para gerenciar centralizadamente os usuários.

2. Estrutura da Árvore e Cadastro de Usuários (LDIF)
A estrutura organizacional foi mapeada em ou=pessoas. O arquivo usuarios.ldif foi devidamente injetado e processado pelo servidor para armazenar os usuários de teste.

Comando de consulta da base:

Bash
ldapsearch -x -b "ou=pessoas,dc=technet,dc=local"
3. Evidências e Testes
Consulta e Listagem da Árvore de Diretórios:
O retorno do comando demonstra a base ativa com o resultado contendo os registros estruturados dos usuários (Ana, Carlos, Julia, Marcos, Bruno) salvos no diretório da empresa.

<img width="878" height="793" alt="p4" src="https://github.com/user-attachments/assets/971e16c2-889e-4ba0-956e-ae2ec74c72f2" />
