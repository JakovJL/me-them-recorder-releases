# Me/Them Recorder Releases

Official Windows installers and update files for Me/Them Recorder.

Source code is maintained in a private repository.

## Quick setup (Windows)

1. Open [Releases](https://github.com/JakovJL/me-them-recorder-releases/releases) and choose the newest release named **Me/Them Recorder ...**.
2. Download and run `MeThemRecorder-<version>-Setup.exe`. Do not download the Local Runtime archive manually - the app installs it when needed.
3. Launch **Me/Them Recorder** from the Start menu. The alpha installer is not code-signed, so Windows SmartScreen may require **More info -> Run anyway**.
4. On the first launch, choose one setup:
   - **Download and enable Local** - private, offline transcription. It requires a supported NVIDIA GPU and downloads the Local Runtime plus a Whisper model.
   - **Later - use Groq** - a smaller setup that works without a local GPU. It requires internet and a Groq API key, and recorded audio is sent to Groq for transcription.
5. In **Settings -> API keys**, add only the keys you need:
   - **Groq** for Groq transcription.
   - **Hugging Face** for Room mode (needed once to download pyannote).
   - **OpenRouter** only for optional summaries and Q&A.
6. Choose **Call** for online calls (microphone = `me`, system audio = `them`) or **Room** for meetings recorded with one microphone. Select your microphone, keep system audio on **Auto** in Call mode, and press **Start**.

Requires Windows 10 22H2 (64-bit) or newer. No separate Python, CUDA Toolkit, or `ffmpeg` installation is needed. Local transcription requires a supported NVIDIA GPU and current driver; Groq works without a local GPU.
