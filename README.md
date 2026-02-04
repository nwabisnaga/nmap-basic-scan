# Nmap Basic Scan

This is an introductory project aimed at understanding five basic Nmap commands commonly used in network scanning.

Projeto introdutório com o objetivo de compreender cinco comandos básicos do Nmap utilizados em varredura de redes. 
Por se tratar de um projeto voltado apenas para testes e aprendizado, foi utilizado o domínio scanme.nmap.org, disponibilizado oficialmente para fins educacionais.

# Tools
- Nmap 7.95
- Linux (Ubuntu)

# Command 1 – Basic Scan: nmap scanme.nmap.org

Performs a basic scan to identify open ports on the target host.

Esse comando realiza uma varredura simples com o objetivo de identificar quais portas estão abertas no host analisado.

<img width="819" height="335" alt="image" src="https://github.com/user-attachments/assets/45449050-9639-4fcd-b798-d74b6849004d" />

. PORT: número da porta e protocolo utilizado (TCP)

. STATE: estado da porta (open, closed ou filtered)

. SERVICE: serviço associado à porta
(explicação linha por linha)

# Command 2 – Fast Scan: nmap -F scanme.nmap.org

Scans a reduced list of the most common ports, making the scan faster.

O parâmetro -F (Fast Scan) é utilizado quando há necessidade de ganhar tempo.
Ele realiza a varredura apenas das portas mais comuns, tornando o processo mais rápido do que um scan completo.

<img width="823" height="270" alt="image" src="https://github.com/user-attachments/assets/05a5f04e-48e8-4775-8b0c-0a5980b3df42" />

Menor quantidade de portas exibidas, resultado mais rápido e util para análises iniciais
(ex l-l)

# Command 3 – Scan Specific Ports: nmap -p 22,80,443,53 scanme.nmap.org

Scans only the specified ports, regardless of their current state.

Esse comando é utilizado quando há necessidade de analisar portas específicas, sejam elas abertas ou fechadas, com o objetivo de verificar seu estado atual.

<img width="821" height="291" alt="image" src="https://github.com/user-attachments/assets/f926a13d-143a-444f-b5b3-e5ef0b85ac08" />

. Porta 22 → SSH

. Porta 80 → HTTP

. Porta 443 → HTTPS

. Porta 53 → DNS
(ex l-l)

# Command 4 – Service Version Detection: nmap -sV scanme.nmap.org

Attempts to identify services and their versions running on open ports.

O parâmetro -sV permite identificar quais serviços estão rodando nas portas abertas, além das versões desses serviços.

<img width="950" height="384" alt="image" src="https://github.com/user-attachments/assets/84b9bee9-d0ed-48a2-a231-dc2ab0d29427" />

. Exemplo: OpenSSH, Apache httpd

Versões ajudam a identificar possíveis vulnerabilidades conhecidas
(ex l-l)

# Command 5 – Default Scripts Scan: nmap -sC scanme.nmap.org

Runs default Nmap scripts to gather additional information.

O parâmetro -sC executa scripts padrão do Nmap nas portas abertas, retornando informações extras como: banners de serviços,chaves SSH, títulos de páginas web e headers HTTP

<img width="822" height="497" alt="image" src="https://github.com/user-attachments/assets/cd41dce3-5e1f-413a-b07f-b0417fb6db37" />

. ssh-hostkey: exibe chaves públicas do serviço SSH

. http-title: mostra o título da página web

. http-server-header: identifica o servidor web utilizado
(ex l-l)

(conclusão)

