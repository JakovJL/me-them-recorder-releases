Native streaming sidecar (MeThemLiveRuntime.exe) for Me/Them Recorder.

- transcribe.cpp pinned at 856d7c10a1a864b900e066b7c9801edf373f5148, built CPU + Vulkan (delay-loaded vulkan-1.dll; falls back to the CPU backend when no vendor driver is present)
- Protocol version 1; manifest capabilities: streaming, multi-session, cpu, offline-context, vulkan
- The offline-context capability lets the Nemotron offline replay start streams with right-context R=13; apps without that optional field keep R=0
- The application verifies the archive SHA-256 from the .index.json before installing