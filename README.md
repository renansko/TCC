## Clonar o projeto

# Guia de Configuração - Projeto TCC

## Estrutura do Projeto
O projeto possui três submódulos:
- `nestjs_google_maps` -> Serviço de mapas (repositório `google_maps`)
- `tcc_front` -> Frontend (repositório `TCC_NEXT_FRONT`)
- `tcc_node` -> Serviço de gerenciamento (repositório `TCC_MANAGEMENT_TRUCK`)

## Configuração dos Submódulos

### 1. Clone o Repositório Principal
```bash
git clone git@github.com:renansko/projeto_principal_TCC.git
cd projeto_principal_TCC

```

## 2. Clone os Submódulos
```bash
git submodule update --init --recursive
```

Para resetar completamente os submódulos
```bash # Remove registros dos submódulos
git submodule deinit -f nestjs_google_maps
git submodule deinit -f tcc_front
git submodule deinit -f tcc_node
```

### Remove do cache do git
```bash
git rm --cached nestjs_google_maps
git rm --cached tcc_front
git rm --cached tcc_node
```

#### Limpa os módulos do .git
```bash
rm -rf .git/modules/nestjs_google_maps
rm -rf .git/modules/tcc_front
rm -rf .git/modules/tcc_node
```

```bash

docker compose up

```

### rodar ambiente no docker back para o mapa
```bash

docker compose exec nestjs_google_maps bash

```

### rodar ambiente no docker front
```bash

docker compose exec front bash

```
