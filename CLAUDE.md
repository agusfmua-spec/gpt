# Guionista de Series virales

Este repo replica un GPT que escribe guiones de reels para series de reto documentado
("Día X de 90"). Respondé siempre en español.

- Para cualquier pedido de guion, del reto o de un día nuevo, seguí el skill
  `.claude/skills/guion-reto/SKILL.md` (también se invoca con `/guion-reto`).
- Datos fijos del reto: `reto/perfil.md`. Guiones aprobados: `reto/dias/`.
- Al aprobarse un guion, guardalo en `reto/dias/dia-NN.md`, y hacé commit y push.
- Para cualquier pedido de carrusel de Instagram, seguí el skill `.claude/skills/carrusel/SKILL.md`
  (también `/carrusel`). Es independiente del reto: marca en `carruseles/marca.md`, fotos en
  `carruseles/fotos/`, fuentes en `carruseles/fuentes/`, cada carrusel en `carruseles/NN-slug/`
  (exportar con `node .claude/skills/carrusel/render.mjs carruseles/NN-slug`). Al aprobarse, commit y push.
- Para usarlo en un Proyecto de claude.ai, ver `PROYECTO_CLAUDE_AI.md`.
- Versión web (Artifact con chat, perfil, estructura y guiones guardados):
  `artifact/guionista-de-retos.html`, publicada en https://claude.ai/artifact/CnfdpbAGLDTyKjBnzJ7F2g
- Versión para alumnas (solo chat y "Mis guiones", estructura fija):
  `artifact/guionista-de-retos-alumnas.html`, publicada en https://claude.ai/artifact/VuCP15MxJMpbBAXywWuRJS.
  Se genera desde `guionista-de-retos.html` cambiando `const ALUMNA = false` a `true` y quitando "Premium"
  del `<title>` y del `<h1>` (la versión de la dueña se llama "Guionista de Series virales Premium"); si cambia la estructura
  por defecto (`DEFAULT_ESTRUCTURA`), regenerarla y volver a publicar las dos.
  La versión de alumnas pide el código de acceso (se compara su SHA-256 en `ACCESS_HASH`).
  Las invitadas no pueden chatear en el link compartido: cada alumna tiene que hacer "Hacer una copia" del
  artifact (así es dueña de la suya). El aviso del chat se lo explica cuando detecta que es invitada.
