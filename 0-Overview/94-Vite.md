# Vite

O Plugin CMMV para Vite permite que o Vite processe arquivos ``.cmmv`` de forma semelhante aos Componentes de Arquivo Único (SFCs) do Vue. Com este plugin, os desenvolvedores podem escrever e usar arquivos ``.cmmv`` diretamente em seus projetos, aproveitando o ambiente de desenvolvimento rápido do Vite.

* **GitHub:** [https://github.com/andrehrferreira/vite-plugin-cmmv](https://github.com/andrehrferreira/vite-plugin-cmmv)

## Instalação

Para usar o Plugin CMMV para Vite, você pode instalá-lo via npm:

```bash
$ pnpm add -D @cmmv/plugin-vite vite @vitejs/plugin-vue vue
```

## Configuração

Para configurar o Vite para reconhecer e processar arquivos ``.cmmv``, siga os passos simples abaixo.

### Passo 1: Adicione o plugin à configuração do Vite

No seu arquivo ``vite.config.js``, importe o plugin e adicione-o ao array ``plugins``:

```javascript
// vite.config.js
import cmmvPlugin from '@cmmv/plugin-vite';

export default {
  plugins: [cmmvPlugin()],
};
```

É tudo o que você precisa para configurar o Vite para interpretar arquivos ``.cmmv``!

### Exemplo de Uso

Aqui está um exemplo de estrutura de arquivo ``.cmmv``. Ele funciona de forma semelhante ao formato de Componentes de Arquivo Único do Vue:

```html
<template>
	<div>{{ message }}</div>
</template>

<script>
export default {
	data() {
		return {
			message: 'Olá CMMV!'
		};
	}
};
</script>

<style>
div {
	color: blue;
}
</style>
```

O arquivo ``.cmmv`` acima consiste em três seções: ``template``, ``script`` e ``style``, que são processadas da mesma forma que os componentes Vue.

### Projeto Exemplo

Para um exemplo prático de como usar o **Plugin CMMV para Vite**, confira o [Projeto CMMV Reactivity](https://github.com/andrehrferreira/cmmv-reactivity). Este projeto demonstra como configurar e usar o plugin em um cenário real, mostrando o poder e a simplicidade de integrar arquivos CMMV em seus projetos baseados em Vite.
