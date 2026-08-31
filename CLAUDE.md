# n2m-rift — notas para Claude Code

## Memoria compartida Zabcom (zabcom-memoria)
Esta carpeta (módulo del juego (rift)) pertenece al proyecto **`n2m`** (Into The Multivers / N2M: videojuego web conectado a Enjin, portal, backend, Unity) en la memoria compartida (MCP `zabcom-memoria`). El backend vivo corre en el server **ENJ 192.168.0.147** (`czb`, stack `n2m-backend`: api :4000 Fastify+TS, worker BullMQ, wallet-daemon de Enjin, redis, postgres; público `n2m.zabcom.net` vía el túnel del 116). El volumen `n2m-wallet-store` es la wallet de Enjin: irreemplazable, nunca borrarlo. El backend del server NO está en git (editar + respaldo tar + rebuild).

- Al iniciar: llama `contexto_proyecto("n2m")` y léelo antes de proponer nada.
- La documentación es punto de partida, no verdad absoluta: verifica en el repo/servidor antes de actuar.
- Al terminar un trabajo: `registrar_terminado` con qué cambió y qué secciones de doc tocaste; si cambió un flujo del juego/economía, el despliegue o un componente, actualízalo con `actualizar_doc` / `guardar_componente`.
- Si algo no está documentado, sigue el flujo de arranque: pregunta al humano, no asumas. Solo el humano confirma (`confirmar_doc`).
- Nunca escribas credenciales, mnemónicos ni llaves de wallets en docs ni bitácora; apunta dónde viven (`.env` en el server ENJ).
- El dueño hace los `git push`; no hacer push automático. Explicaciones cortas.
