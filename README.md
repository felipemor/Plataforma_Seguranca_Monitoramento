
# Plataforma Integrada de Segurança e Monitoramento - Trabalho de conclusão - Mestrado em Cybersecurity

[![Python Version](https://img.shields.io/badge/python-3.11%2B-blue)](https://www.python.org/)
[![Docker](https://img.shields.io/badge/docker-ready-blue)](https://www.docker.com/)
[![OpenSSL](https://img.shields.io/badge/openssl-required-green)](https://www.openssl.org/)

## 📋 Descrição

Solução abrangente de segurança cibernética que oferece monitoramento, análise e resposta automatizada a ameaças em tempo real. A plataforma integra múltiplas funcionalidades de segurança em uma arquitetura unificada.

### ⚡ Funcionalidades Principais

- **🔍 Coleta e Normalização de Logs**: Coleta automatizada de logs de múltiplas fontes (servidores, firewalls, aplicações)
- **🛡️ Análise de Segurança Avançada**: Detecção de ameaças em tempo real (brute-force, SQL Injection, privilege escalation)
- **🔒 Criptografia de Dados**: Proteção de dados sensíveis utilizando algoritmos AES e RSA
- **📜 Gestão de Certificados**: Gerenciamento completo de certificados digitais com OpenSSL
- **⚡ Resposta Automatizada**: Resposta imediata a incidentes com bloqueio de IPs e notificações
- **📊 Dashboards Interativos**: Visualização de dados para governança e compliance
- **🤖 Detecção de Anomalias**: Machine Learning e Deep Learning para detecção proativa de ameaças

## 🛠️ Tecnologias Utilizadas

- **Linguagens**: Python, Bash
- **Containerização**: Docker, Docker Compose
- **Bancos de Dados**: PostgreSQL, MongoDB
- **Machine Learning**: TensorFlow, PyTorch, Scikit-learn
- **Visualização**: Plotly/Dash, Grafana
- **Criptografia**: PyCryptodome, OpenSSL

## 📦 Pré-requisitos

### Sistema Operacional
- Linux (Ubuntu 20.04+ / CentOS 8+)
- macOS 10.15+
- Windows 10/11 (com WSL2 recomendado)

### Dependências

# Docker e Docker Compose
sudo apt-get install docker.io docker-compose

# Python 3.11+
sudo apt-get install python3.11 python3.11-pip

# OpenSSL
sudo apt-get install openssl libssl-dev

# Ferramentas adicionais
sudo apt-get install git make curl
🗂️ Estrutura do Projeto
text
Plataforma_Seguranca_Monitoramento/
│
├── 📁 src/                          # Código fonte principal
│   ├── collectors/                  # Módulos de coleta de logs
│   │   ├── collect_logs.py
│   │   └── log_sources/
│   ├── processors/                  # Processamento e normalização
│   │   ├── normalize_logs.sh
│   │   └── data_processor.py
│   ├── security/                    # Análise de segurança
│   │   ├── security_analysis.py
│   │   └── threat_detection/
│   ├── encryption/                  # Módulos de criptografia
│   │   ├── encryption.py
│   │   └── key_management/
│   ├── certificates/                # Gestão de certificados
│   │   ├── cert_manager.py
│   │   └── ssl_tools/
│   ├── response/                    # Resposta a incidentes
│   │   ├── incident_response.py
│   │   └── automation/
│   ├── visualization/               # Dashboards e visualização
│   │   ├── dashboard.py
│   │   └── reports/
│   └── ml/                          # Machine Learning
│       ├── ml_models.py
│       ├── deep_learning.py
│       └── models/
│
├── 📁 config/                       # Arquivos de configuração
│   ├── config.yaml
│   ├── docker-compose.yml
│   └── environment.env
│
├── 📁 data/                         # Dados e logs
│   ├── raw_logs/
│   ├── processed/
│   └── models/
│
├── 📁 docs/                         # Documentação
│   ├── INSTALL.md
│   ├── API.md
│   └── EXAMPLES.md
│
├── 📁 tests/                        # Testes automatizados
│   ├── test_security.py
│   ├── test_encryption.py
│   └── test_ml.py
│
├── Dockerfile
├── requirements.txt
├── setup.py
└── README.md
🚀 Como Executar
1. Clonar o Repositório

git clone https://github.com/seu-usuario/plataforma-seguranca-monitoramento.git
cd plataforma-seguranca-monitoramento
2. Configurar Ambiente

# Instalar dependências Python
pip install -r requirements.txt

# Configurar variáveis de ambiente
cp config/environment.env.example config/environment.env
# Editar o arquivo com suas configurações
3. Executar com Docker (Recomendado)

# Build e inicialização dos containers
docker-compose up --build -d

# Verificar status
docker-compose logs -f
4. Execução Manual dos Módulos
bash
# Coleta de logs
python src/collectors/collect_logs.py

# Análise de segurança
python src/security/security_analysis.py

# Teste de criptografia
python src/encryption/encryption.py

# Gerenciamento de certificados
python src/certificates/cert_manager.py

# Dashboard interativo
python src/visualization/dashboard.py
⚙️ Configuração
Edite o arquivo config/config.yaml para personalizar a plataforma:


# Configurações de alerta
alert_email: ciso@empresa.com
alert_phone: +5511999999999

# Configurações de banco de dados
database:
  host: localhost
  port: 5432
  name: security_db
  user: admin

# Regras de detecção
detection_rules:
  brute_force:
    max_attempts: 5
    time_window: 300
  sql_injection:
    enabled: true
    sensitivity: high
🧪 Testes
Testes Automatizados

# Executar todos os testes
python -m pytest tests/ -v

# Testes específicos
python -m pytest tests/test_security.py -v
python -m pytest tests/test_encryption.py -v
Testes Manuais

# Testar coleta de logs
python -m src.collectors.collect_logs --test

# Testar criptografia
python -m src.encryption.encryption --test

# Validar certificados
python -m src.certificates.cert_manager --validate
📊 Monitoramento e Dashboard
Acesse o dashboard principal:

# Localmente
http://localhost:8050

# Ou via Grafana
http://localhost:3000
🔧 Desenvolvimento
Adicionando Novas Fontes de Log
Adicione parser em src/collectors/log_sources/

Configure em config/config.yaml

Adicione testes em tests/test_collectors.py

Implementando Novas Regras de Detecção
Edite src/security/threat_detection/rules.py

Atualize configurações no YAML

Adicione testes unitários

🤝 Contribuição
Fork o projeto

Crie sua feature branch (git checkout -b feature/AmazingFeature)

Commit suas mudanças (git commit -m 'Add some AmazingFeature')

Push para a branch (git push origin feature/AmazingFeature)

Abra um Pull Request

📝 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

🆘 Suporte
Para suporte e dúvidas:

📧 Email: fsec.costa@gmail.com

🐛 Issues: GitHub Issues

📚 Documentação: Wiki

⚠️ Importante: Esta é uma plataforma de demonstração. Para uso em produção, implemente medidas adicionais de segurança, auditoria e testes rigorosos.
