# Estudio de Caso: [Strongest Pomodoro Web]

[English version](./strongest-pomodoro-system.md)

## 🎯 Problema

En la búsqueda de métodos para mejorar mi productividad me encontré con el problema de encontrar una aplicación que me permitiera crear los pomodoros suficientes a la vez para terminar mi rutina diaria, sin excederme para hacer mi productividad más sostenible a lo largo del tiempo

## 🧩 Enfoque y Arquitectura

- Arquitectura Feature First, migré el proyecto de la "arquitectura" por defecto de React (arquitectura basada en componentes) a Feature First, lo que después de aproximadamente 2 semanas de trabajo me permitió agregar más funcionalidades de una manera más fácil y rápida, aumentando mi productividad
  ![Arquitectura Feature First](../../img/Architecture/dependency-graph.svg)

- Elección de tecnologías: Next.js por la fácil implementación de paginación y SSR

## 🚧 Retos

- Migrar el proyecto de arquitectura
- La creación del componente con D3.js y la visualización de datos en forma de reloj
- Alinear un diseño complicado con una buena experiencia de usuario
- Crear módulos nativos para React Native
- Que el temporizador pudiera funcionar y evitar el Throttling de pestañas en segundo plano
- Crear un diseño adaptativo (no solo responsivo) teniendo en cuenta que iba a ser una aplicación para web y otra para móvil con comunicación bidireccional [Strongest Pomodoro Web] <-> [Strongest Pomodoro Mobile]

## 🔍 Soluciones

- La migración del proyecto sin duda fue el desafío más difícil al que me enfrenté, era algo que jamás había hecho, pero investigando, con ayuda de diferentes IAs, sobre todo ChatGpt, no solo lo logré, sino que descubrí e implementé la arquitectura más conveniente para el proyecto
- La idea del componente llegó de los diseños HUD mucho antes de pensar en la implementación. Logré implementarlo repasando un poco temas de trigonometría para pasar tiempo a radianes, funcionalidades de D3, dividiendo cada visualización en una pequeña funcionalidad hasta tener el componente completo
- Tuve que encontrar el equilibrio entre no sobrecargar a los usuarios y a la vez no estancarme en un diseño minimalista poco atractivo que pude haber hecho en un día
- La creación de módulos nativos no fue posible, no encontré la manera ni buena documentación para implementarlos en la app móvil, por lo que la app móvil está siendo desarrollada con Kotlin. Aun así, logré resolver un problema ahora señalado en el CLI de Expo [Expo Modules - Bug NPM on trying to npx create-expo-module](https://github.com/expo/expo/issues/20624#issuecomment-2450869207)
- Implementé un web worker encargado de llevar el temporizador (planeo mejorarlo aún más para evitar cualquier problema o que el usuario pueda perder el temporizador)
- La solución ya la había logrado antes, en mis comienzos de desarrollo frontend, todo tiene que ver con usar los vw para la creación de grid columns y grid rows (css). Creé una herramienta para facilitarme el flujo, pensé en hacer un plugin en Figma usando el ruler para hacerlo todo aún más fácil, pero Figma no nos da la capacidad de trabajar con la API del ruler (no hasta el momento julio 2025)

## 📈 Resultados

- Mejora en la capacidad de agregar más código, más funcionalidades, depurar, optimizar, refactorizar
- Hacer una aplicación con un mejor diseño, haciéndola parecer un HUD sci-fi futurista
- Reduje el tiempo de aprendizaje al usar la aplicación, haciéndola muy intuitiva
- Experiencia para no usar React Native para proyectos serios jaja
- Que el temporizador siguiera funcionando mientras trabajaba o estudiaba, ayudando a evitar el agotamiento o la procrastinación

## 🛠️ Próximos Pasos

- Agregar un recorrido por la aplicación
- Agregar anuncios
- Agregar sistemas freemium
- Migrar a TypeScript (por diversión)
- Agregar Playwright
- Mejorar robustez en web
- Integrar un backend en Firebase o Supabase
- Integrar la aplicación móvil
