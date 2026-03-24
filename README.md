# Desafio-DIO---Riachuelo-Cyberseguranca
# Simulação de Ataques em Ambiente Controlado (FTP, Web e SMB)

## Sobre o Projeto

Este projeto apresenta a documentação prática de simulações de ataques em um ambiente de laboratório, com foco em técnicas utilizadas em Testes de Intrusão (Pentest).

O objetivo é demonstrar o processo completo de:

- Reconhecimento
- Enumeração
- Ataques de autenticação
- Validação de acesso
- Análise de riscos
- Recomendações de mitigação

Os testes foram realizados em ambiente **100% controlado**, utilizando máquinas virtuais destinadas ao aprendizado em segurança ofensiva.

---

## Objetivo Geral

Demonstrar, de forma prática e documentada, como serviços expostos e credenciais fracas podem comprometer a segurança de sistemas, evidenciando a importância de boas práticas de proteção.

---

## Ambiente de Laboratório

| Função | Sistema |
|--------|--------|
| Máquina atacante | Kali Linux |
| Máquina alvo | Metasploitable |
| Rede | Host-Only |
| IP do alvo | 192.168.56.102 |

---

## Estrutura do Projeto

Este projeto está dividido em três cenários de ataque:

### Ataque em Serviço FTP

**Técnicas utilizadas:**

- Enumeração de portas com Nmap  
- Identificação de versão vulnerável (vsftpd 2.3.4)  
- Ataque de força bruta com Medusa  
- Validação de acesso e navegação no servidor  

**Riscos identificados:**

- Credenciais fracas  
- Exposição de arquivos  
- Possível movimentação lateral  

📄 Ver relatório completo em: `/ftp_attack`

---

### Ataque em Formulário Web (DVWA)

**Técnicas utilizadas:**

- Análise de requisições HTTP via DevTools  
- Identificação de parâmetros de autenticação  
- Ataque de força bruta automatizado com Hydra  
- Validação de acesso administrativo  

**Riscos identificados:**

- Falta de proteção contra brute force  
- Possível comprometimento da aplicação  
- Exposição de dados sensíveis  

📄 Ver relatório completo em: `/web_attack_dvwa`

---

### Password Spraying em Serviço SMB

**Técnicas utilizadas:**

- Enumeração de usuários com enum4linux  
- Construção de wordlists  
- Password Spraying com Medusa  
- Validação de acesso com smbclient  

**Riscos identificados:**

- Credenciais fracas em rede interna  
- Acesso a compartilhamentos administrativos  
- Possível escalonamento de privilégios  

📄 Ver relatório completo em: `/smb_attack`

---

## Principais Vulnerabilidades Demonstradas

- Uso de senhas fracas ou padrão
- Serviços expostos desnecessariamente
- Falta de limitação de tentativas de login
- Ausência de autenticação multifator
- Exposição de informações via enumeração

---

## Recomendações Gerais de Segurança

- Implementar políticas de senhas fortes
- Utilizar MFA (Autenticação Multifator)
- Monitorar logs e eventos de autenticação
- Restringir exposição de serviços na rede
- Realizar auditorias de segurança periódicas
- Aplicar o princípio do menor privilégio

---

## Ferramentas Utilizadas

- Nmap  
- Medusa  
- Hydra  
- enum4linux  
- smbclient  
- Ferramentas de Desenvolvedor do Navegador  

---

## Habilidades Demonstradas

- Reconhecimento e enumeração de rede  
- Ataques de autenticação (Brute Force e Password Spraying)  
- Análise de protocolos (FTP, HTTP, SMB)  
- Interpretação de resultados técnicos  
- Documentação de testes de segurança  
- Pensamento ofensivo e análise de risco  

---

## Aviso Legal

Este projeto foi realizado exclusivamente para fins educacionais, em ambiente controlado e autorizado.

As técnicas apresentadas **não devem ser utilizadas em sistemas sem permissão formal**.

---

## Autor

Rafael Ribeiro  

Cybersecurity Analyst | Google Cybersecurity Certificate

GitHub: https://github.com/rafaelribeiro-s
LinkedIn: www.linkedin.com/in/rafael-ribeiro-373268294