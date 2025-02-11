# useMotions

useMotions is used to **access** the **motion instances** from v-motion directives **declared** from **templates**.

If you **declare** a **name** using `v-motion` attribute **value**, the **motion instances** will be added to the **global** useMotions **state** and be **accessible** from any **component**.

Be **careful** about **duplicating** the same **name**, note that the **name** can be including a **variable**.

## Exposed

### `{ ...motionControls }`

useMotions exposes an **object** in which **keys** are defined from all the **v-motion** for which you defined a name **value**.

Each values are [**Motion Instances**](/motion-instances) for the named elements.

## Example

```vue
<template>
    <div v-motion="'myName'">
</template>

<script setup>
import { useMotions } from '@vueuse/motions'

const { myName } = useMotions()
</script>
```
