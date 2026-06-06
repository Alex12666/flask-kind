

# Flask Backend - Kubernetes (Kind) & CI/CD Pipeline

Este projeto consiste em uma aplicação de backend desenvolvida em Python com o framework **Flask**, empacotada utilizando boas práticas de **Docker Multi-Stage Build** e orquestrada localmente em um cluster Kubernetes utilizando o **Kind**. 

O projeto também conta com uma esteira de automação (CI/CD) via **GitHub Actions** que valida toda a infraestrutura e a conectividade da aplicação a cada alteração de código.

---

##  Estrutura do Diretório

```text
.
├── .github/
│   └── workflows/
│       └── test-backend.yml  # Esteira de CI automatizada (GitHub Actions)
├── backend/
│   ├── Dockerfile            # Receita Multi-Stage otimizada para produção
│   ├── app.py                # Código fonte da aplicação Flask
│   └── requirements.txt      # Dependências do Python (com versões fixadas)
├── .gitignore                # Filtro de arquivos para evitar tracking de lixo/segredos
├── pod.yaml                  # Manifesto de Pod do Kubernetes
└── README.md                 # Documentação completa do projeto
