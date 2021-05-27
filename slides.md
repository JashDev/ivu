---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
---

# Introducción a la vida universitaria

Bendezu Morales Marco
<br/>
Huamaní Quiñones Noel Alexander
<br/>
Millan Marín Erick Ronaldiño
<br/>
Quispe Carhuancho George Patrick
<br/>
Sifuentes Herrera Jhojhan Antony
<br/>


<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 p-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Presiona espacio para ver la siguiente página <carbon:arrow-right class="inline"/>
  </span>
</div>

<a href="https://github.com/JashDev/ivu" target="_blank" alt="GitHub"
  class="abs-br m-6 text-xl icon-btn opacity-50 !border-none !hover:text-white">
  <carbon-logo-github />
</a>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# ¿Qué hace un profesional de Ingeniería de Sistemas?

- **Redes y telecomunicaciones** - Descripción de lo que se hace en la carrera
- **Desarrollo de software** - Descripción de lo que se hace en la carrera

<br>
<br>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Autoridades de la carrera

```ts {all|1-4|6-9|11-14}
const DirectorCampusHuancayo = {
  name: 'Carlos Alberto',
  lastName: 'Meza Anglas'
}

const DirectorGestiónAcadémica = {
  name: 'Abel Edmundo',
  lastName: 'Juárez Valdivia'
}

const CoordinadorIngenieria = {
  name: 'Ronald Michael',
  lastName: 'Villanueva Añazco'
}
```

<div style="transform: translate(400%, -115%); width: 150px">
<img v-if="$slidev.nav.clicks === 1" border="rounded" src="https://res.cloudinary.com/da1yarvtc/image/upload/v1622063017/director_campus_mdjtmz.png">
<img v-if="$slidev.nav.clicks === 2" border="rounded" src="https://res.cloudinary.com/da1yarvtc/image/upload/v1622063337/director_gestion_fjinzx.png">
<img v-if="$slidev.nav.clicks === 3" border="rounded" src="https://res.cloudinary.com/da1yarvtc/image/upload/v1622063337/coordinador_rjzxxc.png">
</div>

---

<div class="w-60 relative mt-6">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-square.png"
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-circle.png"
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-triangle.png"
    />
  </div>

  <div 
    class="text-5xl absolute top-14 left-40 text-[#2B90B6] -z-1"
    v-motion
    :initial="{ x: -80, opacity: 0}"
    :enter="{ x: 0, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    ENTREVISTAS
  </div>
</div>

<video  v-click="1" width="500" style="margin: auto" controls v-if="$slidev.nav.clicks === 1">
  <source src="https://res.cloudinary.com/da1yarvtc/video/upload/v1622064029/entrevista_ing_nicolas_g4humo.mp4" type="video/mp4">
</video>

<video v-click="2" width="500" style="margin: auto" controls  >
  <source src="https://galaxia-software-test.s3.amazonaws.com/Pruebas/Entrevista.mp4" type="video/mp4">
</video>


<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 0,
  y: 0,
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

---

# ¿Por qué es importante la carrera para la sociedad?

* Permite el desarrollo de tecnologías de información.
* Nos facilita muchos procesos gracias a la interconexión.
* Tiene aplicación en cualquier área.
