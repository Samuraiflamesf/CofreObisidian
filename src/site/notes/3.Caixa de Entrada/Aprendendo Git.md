---
title: Aprendendo Git
created: 2024-09-28
dg-publish: true
tags:
  - pessoal/estudos
  - pessoal/quaseumdev
---
| [Voltar](1.LIFE/index) | [[3.Caixa de Entrada/Git Flow\|Git Flow]] | [[3.Caixa de Entrada/PHP_Artisan\|PHP_Artisan]] |
### **Inicialização do Projeto:**
**Criar um novo repositório Git.**
```bash
git init
```
**Para adicionar todos arquivos e criar um commit**
```bash
git commit -am 'Feat: Enviando email, sobre contatos'
```
**Subindo para nuvem**
```bash
git push origin name_branch
```
****
### Sobre Branch
**Criação de uma Nova Branch:**
```bash
git checkout -b "nome"
```
**Comando para atualizar as branch do projeto:**
```bash
git fetch
```
**Selecionar branch e atualizar:**
```bash
git pull origin nome_da_branch
```
**Comando para atualizar as branch do projeto:**
```bash
git push origin feature/mailtrap-contact
```
#### Baixar versão mais recente da branch
Resolva os conflitos pendentes, conforme descrito anteriormente:
   ```bash
   git status
   ```
Após resolver qualquer conflito ou problema pendente, **descarte as alterações locais** se você não precisar mantê-las:
   ```bash
   git reset --hard
   ```
Certifique-se de estar na branch onde deseja baixar as atualizações:
   ```bash
   git checkout feature/mailtrap-contact
   ```
Agora, faça o **pull** para baixar a versão mais recente da branch remota:
   ```bash
   git pull origin feature/mailtrap-contact
   ```
***
### Setup inicial de projeto Laravel
**Clonando projeto**
```bash
git clone Samuraiflamesf/StudyCMS.git
```
**Copie o arquivo .env.example**
```bash
cp .env.example .env
```
**Instale as dependências e o framework**
```bash
composer install
```
**Crie uma nova chave para a aplicação**
```bash
php artisan key:generate
```
**Rodando migrates**
```bash
php artisan migrate
```
***
**Erro "fatal: remote origin already exists":**
* Esse erro ocorre quando um controle remoto com o mesmo nome já existe.
* Para resolvê-lo, execute:
```bash
git remote rm origin
```
**fatal: not a git repository (or any of the parent directories): .git**
* Para resolvê-lo, execute:
```bash
git init
```
