# RENAI AI Companion Visionary · Prototype 04 (Voice UI Lab)

Mobile-first, no-build UI prototype for GitHub Pages. Designed for editing from Android using QuickEdit.

## Main navigation
Login (`index.html`) leads directly to the chat-first RenAI Companion (`companion.html`). The dedicated call interface is `live.html`; Dashboard (`app.html`) and Pengaturan (`settings.html`) remain secondary destinations.

## Pages
- `index.html`: free demo login. Username required; password is optional and never validated.
- `app.html`: dashboard.
- `companion.html`: main chat page, with separate voice/live call entry points.
- `live.html`: video-call-inspired layout with a large RenAI participant panel, floating local camera preview, microphone meter, browser text-to-speech demo, manual stop, and experimental voice-activity interruption (barge-in) test.
- `settings.html`: tidy settings hub with profile summary, appearance/language, companion, integrations, billing, about, and account.
- `profile.html`: profile editor.
- `router-settings.html`: dedicated RenAI Router preferences page.
- `voice-settings.html`: dedicated voice/microphone preferences page.
- `pricing.html`: mock package pricing.
- `subscription.html`: mock subscription status.
- `payments.html`: payment and invoice placeholder.
- `history.html`: activity placeholder.
- `about.html`: project and UI information.

## Structure
- `css/base/`: theme variables, reset, typography.
- `css/components/`: shared UI elements.
- `css/layout/`: shell layout.
- `css/pages/`: page-specific styles, including login, settings, companion and live view.
- `css/responsive.css`: responsive layout.
- `css/animations.css`: loader and motion.
- `js/modules/`: UI helpers, auth demo state, navigation, loader, theme, language.
- `js/pages/`: login, settings, billing and camera/chat demo behavior.

## Real-time voice UI experiment
- Tap **Mulai mikrofon** to enable the local microphone meter.
- Tap **Uji suara RenAI** to test browser text-to-speech. Speak loudly while the sample voice plays to test automatic interruption; room noise can trigger false positives.
- **Hentikan suara** stops the sample manually.
- This prototype is a local interaction experiment only. A real two-way AI voice session will later require a compatible model/service and a secure connection path.

## GitHub Pages from a phone
1. Download and extract the ZIP.
2. Upload the contents of the `renai-visionary-prototype03` folder to the repository root.
3. GitHub → Settings → Pages → deploy from branch `main`, folder `/ (root)`.
4. Open the HTTPS Pages URL.

## Limits
- Demo login is not authentication; do not enter real passwords.
- Billing prices are mock UI, not official prices or real checkout.
- Camera preview is local browser-only; no video is uploaded.
- Chat is simulated. No AI model or backend is connected.
- The call screen can request camera/microphone permissions. Camera preview stays local. The microphone meter measures local signal energy; when browser speech synthesis is playing, loud mic input can stop the demo speech as an experimental barge-in test. This is not speech recognition or an AI conversation. No audio/video is sent to a model. Audio route choices are preferences only; Android/browser controls physical speaker routing. Browser speech synthesis and microphone access vary by device/browser.
- Language preference is stored, but does not yet translate all UI text.
- Theme preference is stored in localStorage.


### Pembaruan Voice UI Lab
- Panel ringkasan percakapan menampilkan teks sambutan demo.
- Tombol uji suara membacakan sambutan bahasa Indonesia dalam dua paragraf.
- Avatar memiliki efek visual saat audio demo diputar.
- Fitur tetap lokal dan belum terhubung ke backend atau model AI.


### Perbaikan pemutaran suara pada browser mobile
- Uji suara memecah sambutan menjadi dua bagian agar lebih andal pada beberapa browser Android.
- Mencoba memilih voice bahasa Indonesia bila tersedia.
- Pesan status yang lebih jelas jika fitur TTS tidak tersedia atau gagal diputar.
- Tetap memakai Text-to-Speech browser; tidak ada AI voice/backend sungguhan.


### Video-call layout upgrade
- Kamera pengguna menjadi panel utama layar video call.
- Avatar RenAI tampil sebagai picture-in-picture kecil di sudut kanan atas.
- Ketika demo TTS berbicara, jendela RenAI mendapat pulse glow dan animated ring.
- Animasi menunjukkan status demo playback, bukan gerakan bibir AI atau video AI sungguhan.


### Camera orientation and full-width fix
- Removed horizontal mirroring from the main camera preview so environmental left/right orientation follows the camera feed.
- Main camera surface and video element now explicitly fill the full video stage width and height.
- `object-fit: cover` remains enabled; depending on the camera aspect ratio, slight cropping may occur to fill the stage.


### Public voice presentation
- Replaced the personal-name greeting with a neutral, public-facing introduction to RENAI AI Companion Visionary.
- Updated the introduction to explain the prototype and its current limitations clearly.
- Adjusted speech rate and pitch for a calmer presentation and prefers an installed Indonesian system voice when available.
- Naturalness depends on the Indonesian voice installed in the browser/device; this remains browser TTS, not a dedicated neural voice model.


### Public voice script visibility
- The full public introduction remains in the speech synthesis script.
- The transcript panel is hidden from the main call UI, so visitors hear the introduction without seeing the full text displayed in the content area.
