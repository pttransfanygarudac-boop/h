# RENAI AI Companion Visionary · Prototype 04

Mobile-first, no-build UI prototype for GitHub Pages. Designed for editing from Android using QuickEdit.

## Main navigation
Login (`index.html`) leads directly to the chat-first RenAI Companion (`companion.html`). The dedicated call interface is `live.html`; Dashboard (`app.html`) and Pengaturan (`settings.html`) remain secondary destinations.

## Pages
- `index.html`: free demo login. Username required; password is optional and never validated.
- `app.html`: dashboard.
- `companion.html`: main chat page, with separate voice/live call entry points.
- `live.html`: dedicated call-style screen with mute, end-call, and audio-route preference menu.
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
- The call screen can request microphone permission and mute its local track, but no audio is sent to an AI model. Audio route choices are preferences only; Android/browser controls physical speaker routing.
- Language preference is stored, but does not yet translate all UI text.
- Theme preference is stored in localStorage.
