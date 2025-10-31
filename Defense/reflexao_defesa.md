# Reflexão sobre Defesa e Prevenção de Ameaças Digitais

## 🧩 Introdução
Os exercícios de **Ransomware Simulado** e **Keylogger Simulado** permitem compreender, na prática, o funcionamento de duas das ameaças mais recorrentes no cenário de cibersegurança.  
A experiência de implementá-las em ambiente controlado revela não apenas as técnicas utilizadas por agentes maliciosos, mas também a importância de adotar **estratégias preventivas, medidas de mitigação** e **boas práticas de defesa**.

---

## 🔒 1. Medidas de Prevenção

A prevenção é a primeira e mais importante linha de defesa. O objetivo é **evitar que a ameaça se instale** no sistema.

### 🔹 Antivírus e Antimalware
- Utilizar soluções atualizadas com varredura em tempo real.  
- Configurar verificações automáticas e atualização diária das assinaturas.  
- Analisar arquivos baixados de fontes desconhecidas antes da execução.

### 🔹 Firewall
- Manter o firewall do sistema operacional e da rede sempre ativo.  
- Restringir portas e protocolos não utilizados.  
- Monitorar logs de tráfego para identificar comunicações suspeitas.

### 🔹 Controle de Acesso e Privilégios
- Aplicar o princípio do **menor privilégio**: usuários e aplicações só devem ter as permissões necessárias.  
- Bloquear a execução de scripts em diretórios sensíveis (como *Downloads* e *AppData*).  
- Implementar autenticação multifator (MFA) para acesso remoto.

### 🔹 Atualizações e Patches
- Manter o sistema operacional e softwares sempre atualizados.  
- Automatizar o processo de atualização para reduzir janelas de vulnerabilidade.

---

## 🧠 2. Medidas de Mitigação

Quando a prevenção falha, é essencial limitar os danos e restaurar o ambiente com rapidez.

### 🔹 Backup e Recuperação
- Adotar **backup 3-2-1**: três cópias, em dois tipos de mídia, sendo uma fora da rede principal.  
- Testar periodicamente a restauração dos backups.  
- Manter versões históricas de arquivos para mitigar ataques de ransomware.

### 🔹 Sandboxing e Isolamento
- Utilizar máquinas virtuais ou containers para testar arquivos e scripts suspeitos.  
- Separar ambientes de produção e teste, evitando impacto direto nos sistemas críticos.

### 🔹 Monitoramento e Detecção
- Empregar ferramentas de **IDS/IPS (Intrusion Detection/Prevention Systems)**.  
- Registrar logs detalhados de atividades e acessos para auditoria.  
- Configurar alertas para comportamentos anômalos (ex.: picos de CPU, acessos fora do horário usual).

---

## 👥 3. Boas Práticas do Usuário

O fator humano continua sendo o elo mais vulnerável. A conscientização é tão vital quanto as ferramentas técnicas.

- Desconfiar de links, anexos e mensagens não solicitadas.  
- Verificar remetentes antes de abrir e-mails suspeitos.  
- Evitar reutilizar senhas e usar gerenciadores seguros.  
- Participar de treinamentos regulares sobre segurança digital.  
- Utilizar autenticação multifator em todos os serviços críticos.

---

## 🧩 4. Conclusão

O aprendizado obtido ao simular o comportamento de **malwares controlados** — como o ransomware e o keylogger — reforça que **a segurança não depende apenas de tecnologia**, mas também de **processos e pessoas**.  
A defesa eficaz combina **prevenção, mitigação e conscientização**, transformando o conhecimento ofensivo em ferramentas para fortalecer a proteção digital.

---

📘 **Autor:** Angélica França  
📅 **Projeto:** Santander CiberSegurança 2025 