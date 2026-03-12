Aqui está um **guia em Markdown (.md)** organizado e limpo para seguir o passo a passo de criação do projeto Angular com Tailwind e Angular Material.

---

# Guia de Setup – Projeto Angular + Tailwind + Angular Material

Este guia descreve o processo para criar e configurar um projeto Angular com **TailwindCSS** e **Angular Material**, além de simplificar o template inicial.

---

# 1. Instalar Angular CLI globalmente

```bash
npm install -g @angular/cli
```

Verifique a instalação:

```bash
ng version
```

---

# 2. Criar o projeto Angular

```bash
ng new projeto-angular
```

Entrar na pasta do projeto:

```bash
cd projeto-angular
```

---

# 3. Criar o repositório Git

Dentro da pasta do projeto:

```bash
git init
git add .
git commit -m "Projeto Angular inicial"
```

---

# 4. Instalar TailwindCSS

Documentação oficial:
[https://angular.dev/guide/tailwind](https://angular.dev/guide/tailwind)

Instalar dependências:

```bash
npm install tailwindcss @tailwindcss/postcss postcss
```

---

# 5. Criar configuração do PostCSS

Criar manualmente o arquivo:

```
.postcssrc.json
```

Conteúdo:

```json
{
  "plugins": {
    "@tailwindcss/postcss": {}
  }
}
```

---

# 6. Importar Tailwind no projeto

Editar o arquivo:

```
src/styles.css
```

Adicionar:

```css
@import "tailwindcss";

body {
  background-color: #111;
  color: white;
}
```

---

# 7. Instalar Angular Material

Página do pacote:
[https://www.npmjs.com/package/@angular/material](https://www.npmjs.com/package/@angular/material)

Instalar dependência:

```bash
npm i @angular/material
```

---

# 8. Iniciar o projeto

```bash
npm start
```

ou

```bash
ng serve
```

---

# 9. Simplificar template padrão do Angular

### Substituir

```
src/app/app.html
```

por:

```html
<h1>Minha App</h1>
```

---

# 10. Ajustar arquivo `app.ts`

No arquivo:

```
src/app/app.ts
```

Comentar elementos não utilizados:

* RouterOutlet
* signal `title`

Exemplo simplificado:

```ts
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.html',
  styleUrl: './app.css'
})
export class App {
  // title = signal('projeto-angular')
}
```

---

# 11. Remover testes unitários

Apagar o arquivo:

```
src/app/app.spec.ts
```

---

# 12. Abrir ajuda do Angular CLI

Em outro terminal do VS Code:

```bash
ng g --help
```

Isso mostra todos os **geradores disponíveis**:

* components
* services
* guards
* modules
* etc

---

# 13. Criar novo componente de página

Executar:

```bash
ng g c components/shared/page --skip-tests
```

Arquivos criados:

```
src/app/components/shared/page/
page.ts
page.html
page.css
```

---

# 14. Criar template do componente Page

Editar:

```
page.html
```

Exemplo simples:

```html
<div class="p-10 text-3xl">
  Página inicial
</div>
```

---

# 15. Atualizar `app.html`

Editar:

```
src/app/app.html
```

Adicionar:

```html
<app-page></app-page>
```

---

# 16. Atualizar `app.ts`

Importar o componente `Page`.

Exemplo:

```ts
import { Component } from '@angular/core';
import { Page } from './components/shared/page/page';

@Component({
  selector: 'app-root',
  imports: [Page],
  templateUrl: './app.html',
  styleUrl: './app.css'
})
export class App {}
```

---

# Estrutura final esperada

```
projeto-angular
 ├─ src
 │  ├─ app
 │  │  ├─ components
 │  │  │  └─ shared
 │  │  │     └─ page
 │  │  │        ├─ page.ts
 │  │  │        ├─ page.html
 │  │  │        └─ page.css
 │  │  ├─ app.ts
 │  │  └─ app.html
 │  └─ styles.css
 │
 ├─ .postcssrc.json
 └─ package.json
```

---

# Observações

Alterações realizadas no projeto:

* README atualizado com instruções do **Tailwind**
* Template padrão do Angular removido
* `app.html` simplificado
* `app.spec.ts` removido
* `RouterOutlet` e `title signal` comentados
* Tailwind configurado no `styles.css`
* Novo componente `Page` criado

---

✅ Projeto agora pronto para começar o desenvolvimento.

---

Se quiser, posso também te entregar uma versão **melhor ainda desse guia**, com:

* diagrama da estrutura do projeto
* comandos Angular mais usados (`ng g`, `ng add`, etc)
* boas práticas para projetos Angular grandes.
