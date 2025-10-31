<!-- README START -->

# 🧠 Desafio Prático — Simulação de Malware com Python (Ransomware e Keylogger)

> Projeto prático de Cibersegurança proposto pela DIO, com o objetivo de **demonstrar o funcionamento de Ransomware e Keylogger em ambiente controlado**, utilizando **Python**, para compreender o comportamento dessas ameaças e estudar **métodos de defesa e mitigação**.

---

## 📘 Sumário

- [🧠 Desafio Prático — Simulação de Malware com Python (Ransomware e Keylogger)](#-desafio-prático--simulação-de-malware-com-python-ransomware-e-keylogger)
  - [📘 Sumário](#-sumário)
  - [📖 Visão Geral](#-visão-geral)
  - [🎯 Objetivos do Projeto](#-objetivos-do-projeto)
  - [🧩 Ambiente Seguro e Ético](#-ambiente-seguro-e-ético)
  - [⚙️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
  - [1️⃣ Ransomware Simulado](#1️⃣-ransomware-simulado)
    - [Etapas de Implementação (SAR)](#etapas-de-implementação-sar)
    - [Fluxo do Script](#fluxo-do-script)
  - [2️⃣ Keylogger Simulado](#2️⃣-keylogger-simulado)
    - [Etapas de Implementação (SAR)](#etapas-de-implementação-sar-1)
    - [Fluxo do Script](#fluxo-do-script-1)
  - [🛡️ Medidas de Defesa e Mitigação](#️-medidas-de-defesa-e-mitigação)
  - [📂 Estrutura Recomendada de Pastas](#-estrutura-recomendada-de-pastas)

---

## 📖 Visão Geral

Este repositório documenta e demonstra **duas simulações de malware** em ambiente **local e controlado**, com propósitos **educacionais**:

1. **Ransomware Simulado:** criptografa e descriptografa arquivos de teste, simulando a lógica de sequestro de dados e mensagem de resgate.  
2. **Keylogger Simulado:** captura teclas digitadas e registra em arquivo `.txt`, podendo realizar envio automatizado via e-mail.

O objetivo principal é **compreender os mecanismos de ataque e suas defesas**, e **reforçar boas práticas de segurança da informação**.

---

## 🎯 Objetivos do Projeto

- Demonstrar o funcionamento básico de Ransomware e Keylogger em Python.  
- Aprender técnicas de **criptografia, manipulação de arquivos e automação de rede**.  
- Compreender **como essas ameaças agem** e como **podem ser detectadas e mitigadas**.  
- Reforçar **a importância de ambientes seguros e testes éticos**.  
- Registrar documentação técnica clara para portfólio e aprendizado.

---

## 🧩 Ambiente Seguro e Ético

- Execução **apenas em ambiente controlado e desconectado da internet**, com arquivos de teste sem valor real.  
- **Proibido** o uso desses scripts fora de ambiente laboratorial.  
- Sistema isolado por **máquina virtual (VM)** é altamente recomendado.  
- Todos os exemplos têm **fins exclusivamente educacionais**.

---

## ⚙️ Tecnologias Utilizadas

| Ferramenta | Finalidade |
|-------------|-------------|
| **Python 3.x** | Linguagem principal |
| **cryptography (Fernet)** | Criptografia simétrica no Ransomware |
| **pynput / keyboard** | Captura de teclas no Keylogger |
| **smtplib** | Envio de logs por e-mail |
| **GitHub** | Documentação e versionamento |

---

## 1️⃣ Ransomware Simulado

### Etapas de Implementação (SAR)

**Situação:** Necessidade de simular o comportamento de um ransomware real sem causar danos.  
**Ação:**  
1. Criar pasta com **arquivos de teste (.txt, .jpg, .pdf)**.  
2. Implementar script Python que:  
   - Gera uma **chave de criptografia**.  
   - Criptografa os arquivos da pasta.  
   - Exibe mensagem de “resgate” com instruções para descriptografar.  
3. Criar função inversa para **descriptografar** os arquivos.  

**Resultado:** Arquivos testados são criptografados e descriptografados corretamente, sem danos permanentes.

**Observação:** Não foi colocado no versionamento o arquivo chave para descriptografia.

---

### Fluxo do Script

1. Gerar chave com módulo `cryptography.fernet`.  
2. Ler e criptografar cada arquivo do diretório alvo.  
3. Exibir mensagem simulando um “resgate”.  
4. Rodar script de descriptografia (com a chave) para restaurar os dados.

---

## 2️⃣ Keylogger Simulado

### Etapas de Implementação (SAR)

**Situação:** Demonstrar o funcionamento de um keylogger simples, para estudo de prevenção e detecção.  
**Ação:**  
1. Utilizar biblioteca `pynput` para capturar teclas.  
2. Armazenar logs em arquivo `.txt`.  
3. Opcional: implementar envio de logs via e-mail com `smtplib`.  
4. Tornar o script “furtivo” (minimizar alertas e execução em segundo plano).  

**Resultado:** As teclas digitadas são gravadas em um arquivo local e, opcionalmente, enviadas automaticamente por e-mail (em ambiente isolado).

---

### Fluxo do Script

1. Monitoramento de eventos de teclado.  
2. Registro contínuo das teclas pressionadas.  
3. Escrita em arquivo `.txt` seguro.  
4. (Opcional) Envio de logs por e-mail simulado.

---

## 🛡️ Medidas de Defesa e Mitigação

1. **Antivírus atualizado:** detecta padrões de comportamento de keyloggers e ransomwares.  
2. **Firewall ativo:** bloqueia conexões suspeitas de saída (exfiltração de dados).  
3. **Sandboxing:** executa arquivos suspeitos em ambiente controlado para análise.  
4. **Backup recorrente:** evita perda de dados em caso de criptografia maliciosa.  
5. **Conscientização do usuário:** principal linha de defesa contra engenharia social.  
6. **Controle de privilégios:** usuários sem privilégios administrativos limitam danos.  
7. **Monitoramento de logs e processos:** detecta anomalias de execução.  

---

## 📂 Estrutura Recomendada de Pastas

```bash
/Malware/
├─ ransoware.py
├─ decrypt.py
├─ test_files/
│ ├─ dados_confidenciais.txt
│ └─ senhas.jpg
├─ LEIA ISSO.txt
/Keylogger/
├─ keylogger.py
├─ log.txt
├─ keylogger_email.py
/Defense/
└─ reflexao_defesa.md
/Images/
└─ evidencias.png
```
