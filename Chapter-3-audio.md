# 🎧 Chapter 3 · Audio & Speech (Introduction Only)

![Scope](https://img.shields.io/badge/Scope-Introduction_only-ff69b4?style=for-the-badge)
![Focus](https://img.shields.io/badge/Focus-Audio_%26_Speech_Workflows-1E90FF?style=for-the-badge)
![Language](https://img.shields.io/badge/Language-English-2ea44f?style=for-the-badge)
![Hardware](https://img.shields.io/badge/Hardware-Mic_recommended-FFA500?style=for-the-badge)
[![Text Chapter](https://img.shields.io/badge/Chapter%201-Text%20Creation-34D399?style=for-the-badge)](./Chapter-1-text.md)
[![Visuals Chapter](https://img.shields.io/badge/Chapter%202-Visuals-8A2BE2?style=for-the-badge)](./Chapter-2-visuals.md)
[![Glossary](https://img.shields.io/badge/Glossary-Quick-FFB020?style=for-the-badge)](#glossary-quick)

This chapter focuses on AI-assisted audio: speech-to-text (STT), text-to-speech (TTS), voice cloning, restoration, diarization, alignment, music generation, and podcast pipelines. Introduction-only with practical workflows and a curated project list.

---

## 💡 What AI Helps With
- Speech transcription (STT), translation, and summarization
- Natural TTS with controllable voice, prosody, and speed
- Voice conversion and cloning for consistent narration
- Noise removal, dereverb, and audio restoration
- Speaker diarization and forced alignment for editing
- Music generation and sound design for backgrounds and SFX
- Podcast/video workflows: recording, mixing, mastering, publishing

## ✅ Recommended Projects (by Use)

### 🗣️ Speech-to-Text (STT)
- [OpenAI Whisper](https://github.com/openai/whisper) — high-quality STT; strong multilingual support  
  - [faster-whisper](https://github.com/SYSTRAN/faster-whisper) — fast CTranslate2 inference  
  - [whisper.cpp](https://github.com/ggerganov/whisper.cpp) — efficient CPU inference
- [Vosk](https://alphacephei.com/vosk/) — offline STT with lightweight models
- Cloud STT (for production latency/cost trade-offs): [Deepgram](https://deepgram.com/), [AssemblyAI](https://www.assemblyai.com/), [Google Speech-to-Text](https://cloud.google.com/speech-to-text)

### 🔊 Text-to-Speech (TTS)
- [Coqui TTS](https://coqui.ai/) — open-source TTS; multi-speaker and fine-tuning
- [Bark (Suno)](https://github.com/suno-ai/bark) — zero-shot multilingual TTS
- [Piper](https://github.com/rhasspy/piper) — fast lightweight TTS for embedded/offline use
- Commercial options: [ElevenLabs](https://elevenlabs.io/), [Amazon Polly](https://aws.amazon.com/polly/)

### 🧑‍🎤 Voice Conversion & Cloning
- [RVC (Retrieval-based Voice Conversion)](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) — popular voice conversion
- [so-vits-svc](https://github.com/svc-develop-team/so-vits-svc) — singing/voice conversion
- [fish-speech](https://github.com/fishaudio/fish-speech) — open-source voice synthesis

### 🛠️ Editing, Restoration, and Enhancement
- [RNNoise](https://github.com/xiph/rnnoise) — real-time noise suppression
- [Demucs](https://github.com/facebookresearch/demucs) — source separation (music, vocals)
- [Spleeter](https://github.com/deezer/spleeter) — music source separation
- [iZotope RX](https://www.izotope.com/en/products/rx.html) — professional restoration (commercial)
- [ffmpeg](https://ffmpeg.org/) — universal audio tooling: resample, normalize, filter

### 👥 Diarization & Alignment
- [pyannote.audio](https://github.com/pyannote/pyannote-audio) — speaker diarization, segmentation
- [aeneas](https://github.com/readbeyond/aeneas) — forced alignment (text ↔ audio)
- [Gentle](https://github.com/lowerquality/gentle) — robust forced alignment (Kaldi-based)

### 🎵 Music & SFX Generation
- [AudioCraft (MusicGen)](https://github.com/facebookresearch/audiocraft) — text-to-music generation
- [Stable Audio](https://stability.ai/stable-audio) — commercial text-to-music
- [Riffusion](https://github.com/riffusion/riffusion) — diffusion-based music from spectrograms
- [Freesound](https://freesound.org/) — large community SFX library (check licenses)

### 🎙️ Recording, Editing & Publishing
- [OBS Studio](https://obsproject.com/) — recording and streaming
- [Audacity](https://www.audacityteam.org/) — open-source audio editor
- [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve) — editing, grading, finishing for video/podcasts
- [Auphonic](https://auphonic.com/) — automatic leveling, loudness, and mastering (cloud)

---

## 🧰 Minimal Viable Stack (Low Barrier)
- Whisper (faster-whisper/whisper.cpp) for transcription
- Piper or Coqui TTS for natural speech
- RNNoise for quick noise suppression
- ffmpeg for resampling, normalization, and conversion

## 🚀 Advanced Stack (More Capabilities)
- pyannote.audio for diarization; aeneas/Gentle for alignment
- Coqui TTS fine-tuning for brand voice; RVC for voice conversion
- Demucs/Spleeter for stems; iZotope RX for restoration
- AudioCraft or Stable Audio for background music generation

## 🔧 Selection Tips
- Latency vs quality: cloud STT/TTS is fast; local offers privacy and control
- Licensing: verify model/asset licenses for commercial use; track sources
- Language support: Whisper handles many languages; check TTS voices for consistency
- Reproducibility: script pipelines (ffmpeg, pyannote, aeneas) and save parameters
- Loudness & delivery: target EBU R128 or platform-specific norms (use ffmpeg `loudnorm`)

## 🗂️ Example Workflow (Adjust as Needed)
1. Record clean audio (OBS); capture room tone; keep consistent mic distance
2. Pre-process: `ffmpeg` resample; RNNoise for noise; optional dereverb
3. Transcribe with Whisper; diarize with pyannote.audio; align key segments with aeneas
4. Edit transcript; regenerate pick-ups via TTS or voice conversion (RVC)
5. Mix/master: level speech, add background music (AudioCraft/Stable Audio), normalize loudness
6. Export: deliver WAV/FLAC masters and platform-specific MP3/MP4 with `loudnorm`

## 📗 Glossary (Quick)
- STT — speech-to-text transcription
- TTS — text-to-speech synthesis
- VAD — voice activity detection
- Diarization — who spoke when
- Forced alignment — align text to audio timestamps
- Voice conversion — transform one voice into another
- Loudness normalization — consistent perceived volume (EBU R128)

## ℹ️ Notes
- This chapter is introduction-only and will evolve with practical workflows.
- For best performance, use recent GPUs; for offline/low-power, prefer Piper and whisper.cpp.

## 🙌 Support
[![Support](https://img.shields.io/badge/Support-Ko--fi-FF5E5B?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/A0A21P7W2J)