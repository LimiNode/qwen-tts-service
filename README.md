# qwen-tts-service
Local WebSocket TTS service built on qwen3-tts-bridge-cpp for persistent streaming synthesis, cancellation, and realtime clients.

This project is the service layer. It does not implement TTS inference itself.

```
LLM / Unity / client
        ↓ WebSocket
qwen-tts-service
        ↓
qwen3-tts-bridge-cpp
        ↓
qwen_tts_native_worker
        ↓
qwen.dll / qwentts.cpp
```

Scope будущего проекта:

- localhost WebSocket API;
- persistent Bridge instance;
- synthesis/cancellation;
- binary streaming PCM;
- client sessions;
- bounded output queues / slow-client policy;
- health/capabilities;
- later Unity client support.
