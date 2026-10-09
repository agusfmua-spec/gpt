# Guionista de Series virales

Este repo replica un GPT que escribe guiones de reels para series de reto documentado
("Día X de 90"). Respondé siempre en español.

- Para cualquier pedido de guion, del reto o de un día nuevo, seguí el skill
  `.claude/skills/guion-reto/SKILL.md` (también se invoca con `/guion-reto`).
- Datos fijos del reto: `reto/perfil.md`. Guiones aprobados: `reto/dias/`.
- Al aprobarse un guion, guardalo en `reto/dias/dia-NN.md`, y hacé commit y push.
- Para usarlo en un Proyecto de claude.ai, ver `PROYECTO_CLAUDE_AI.md`.
- Versión web (Artifact con chat, perfil, estructura y guiones guardados):
  `artifact/guionista-de-retos.html`, publicada en https://claude.ai/artifact/CnfdpbAGLDTyKjBnzJ7F2g
- Versión para alumnas (solo chat y "Mis guiones", estructura fija):
  `artifact/guionista-de-retos-alumnas.html`, publicada en https://claude.ai/artifact/VuCP15MxJMpbBAXywWuRJS.
  Se genera desde `guionista-de-retos.html` cambiando `const ALUMNA = false` a `true`; si cambia la estructura
  por defecto (`DEFAULT_ESTRUCTURA`), regenerarla y volver a publicar las dos.
