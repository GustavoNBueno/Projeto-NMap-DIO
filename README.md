# Projeto-NMap-DIO
Este projeto foi desenvolvido como parte do bootcamp da DIO, com o objetivo de aplicar na prática conceitos de pentest e segurança ofensiva. A atividade consiste em simular um ataque de força bruta (brute force) contra o serviço FTP, utilizando o Kali Linux como máquina atacante e o Metasploitable como ambiente alvo intencionalmente vulnerável.
O objetivo é demonstrar, em um ambiente totalmente controlado e isolado, como credenciais fracas podem ser exploradas por ferramentas automatizadas, reforçando a importância de boas práticas de segurança como senhas fortes, bloqueio de tentativas e autenticação em múltiplos fatores.

🎯 Objetivos
Compreender o funcionamento de ataques de força bruta;
Praticar o uso de ferramentas de pentest em ambiente de laboratório;
Identificar vulnerabilidades relacionadas a autenticação fraca no serviço FTP;
Documentar o processo seguindo boas práticas de um relatório de pentest.
🛠️ Ferramentas utilizadas
Kali Linux – distribuição focada em testes de segurança;
Metasploitable 2 – máquina virtual propositalmente vulnerável para fins educacionais;
Nmap – para reconhecimento e identificação de portas e serviços ativos (incluindo o FTP);
Medusa – para automação do ataque de força bruta contra o serviço FTP;
VirtualBox – para virtualização do ambiente de laboratório.
🧪 Ambiente de testes

⚠️ Este projeto foi executado exclusivamente em ambiente de laboratório isolado (rede interna/host-only), com máquinas virtuais criadas especificamente para fins de estudo. Nenhum sistema real ou de terceiros foi atacado.

Máquina atacante: Kali Linux
Máquina alvo: Metasploitable
Rede: isolada (host-only / NAT interno)
📋 Etapas realizadas
Configuração do ambiente virtual (Kali + Metasploitable em rede isolada);
Escaneamento de portas e serviços com Nmap, identificando o serviço FTP ativo e sua porta;
Preparação de wordlists de usuários e senhas para o ataque;
Execução do ataque de força bruta contra o serviço FTP utilizando o Medusa;
Obtenção de credenciais válidas de acesso ao serviço;
Documentação dos resultados e evidências (prints/logs dos comandos executados).
💻 Exemplo de comandos utilizados
bash
# Escaneamento de portas e serviços
nmap -sV -p 21,22,80,445,139 192.168.56.101

# Ataque de força bruta ao serviço FTP com Medusa
medusa -h 192.168.56.101 -U users.txt -P pass.txt -M ftp -t 6


📎 Resultados

Foi possível obter acesso válido ao serviço FTP utilizando a ferramenta Medusa, evidenciando o uso de credenciais fracas no ambiente Metasploitable.

⚠️ Aviso Legal

Este projeto tem finalidade exclusivamente educacional, desenvolvido em ambiente de laboratório próprio e isolado. A prática de ataques de força bruta ou qualquer técnica de invasão sem autorização expressa é crime previsto em lei (Lei nº 12.737/2012 e Lei Geral de Proteção de Dados). O autor não se responsabiliza pelo uso indevido das informações aqui apresentadas.

👤 Autor

Projeto desenvolvido por Gustavo Bueno como parte do bootcamp de Cybersecurity da DIO.
