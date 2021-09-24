Este repositório tem como objetivo mostrar a configuração básica de um "projeto" TS.
A medida em que for aprimorando minhas habilidades em desenvolvimento web e aprendendo a utilidade de novas ferramentas, irei adicionar aqui.
Qualquer critica ou sugestão de mudanças são bem vindas.


![área](https://user-images.githubusercontent.com/69372682/134607963-7b2d4056-ab28-4a5c-b84b-20a49b71253b.gif)


## Projeto - template_projeto_
1) plugins vscode: eslint prettier, eslint, editorconfig.
	configurar - ctrl + shift + p
	preferences open user
	onsave
	[x] editor format on save
--------------------------------------------------------------
2) criar arquivo editor config.
root = true
indent_style = space
indent_size = 2
end_of_line = lf
charset = utf-8
trim_trailing_whitespace = false
insert_final_newline = false
------------------------------------------------------------------
3) git init
	criar git ignore
-----------------------------------------------------------------
4) yarn init -y
-----------------------------------------------------------------
5) instalar typescript
	yarn add -D typescript
--------------------------------------------------------------------
6) yarn tsc --init, ou criar manualmente tsconfig.json
{"compilerOptions": {
  "target": "es2019",
  "module": "commonjs",
  "allowJs": true,
  "esModuleInterop": true,
  "skipLibCheck": true,
  "forceConsistentCasingInFileNames": true,
  "outDir": "./dist"
}}
-------------------------------------------------------------------
7) yarn add -D eslint
	yarn eslint --init
	responder as perguntas, instalar o que for preciso com npm
	após ter instalado excluir package-lock e yarn.lock
	Depois rodar yarn no cmd novamente para criar um novo yarn.lock
--------------------------------------------------------------------------
8) configurar arquivo .eslintrc.json
	adicionar "prettier" em "extends" e "plugins"
	adicionar "prettier/prettier": "error" em "rules"
----------------------------------------------------------------------------
9) montar um projeto express
	yarn add express
	criar um diretorio src
	criar um server.ts
------------------------------------------------------------------------------
10) montar ambiente de desenvolvimento type script
	yarn add -D ts-node-dev
	criar arquivos de variavies de ambiente .env.local e .env
	yarn add -D dotenv
	adicionar em package.json abaixo de MIT
		"scripts": {
    "dev": "ts-node-dev -r dotvenv/config ./src/server.ts",
    "build" : "tsc"
  },
------------------------------------------------------------------------------
