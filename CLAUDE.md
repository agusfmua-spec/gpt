# Guionista de retos

Este repo replica un GPT que escribe guiones de reels para series de reto documentado
("Día X de 90"). Respondé siempre en español.

- Para cualquier pedido de guion, del reto o de un día nuevo, seguí el skill
  `.claude/skills/guion-reto/SKILL.md` (también se invoca con `/guion-reto`).
- Datos fijos del reto: `reto/perfil.md`. Guiones aprobados: `reto/dias/`.
- Al aprobarse un guion, guardalo en `reto/dias/dia-NN.md`, y hacé commit y push.
- Para usarlo en un Proyecto de claude.ai, ver `PROYECTO_CLAUDE_AI.md`.
