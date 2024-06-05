# Componentes

Os arquivos de modelo Vue nesta pasta são importados automaticamente.

## 🚀 Uso

A importação é feita por [unplugin-vue-components](https://github.com/unplugin/unplugin-vue-components). Este plugin importa automaticamente arquivos `.vue` criados no diretório `src/components` e os registra como componentes globais. Isso significa que você pode usar qualquer componente em seu aplicativo sem precisar importá-lo manualmente.

O exemplo a seguir assume um componente localizado em `src/components/MyComponent.vue`:

```vue
<template>
  <div>
    <MyComponent />
  </div>
</template>

<script lang="ts" setup>
  //
</script>
```
Quando seu modelo for renderizado, a importação do componente será automaticamente incorporada, o que será renderizado assim:

```vue
<template>
  <div>
    <MyComponent />
  </div>
</template>

<script lang="ts" setup>
  import MyComponent from '@/components/MyComponent.vue'
</script>
```
