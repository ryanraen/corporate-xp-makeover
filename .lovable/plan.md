# Build the 9to5 corporate desktop game

## Goal
Turn the Windows XP template into a playable, desktop-only satire of corporate work while preserving the template’s strongest visual and interaction patterns.

## What will be built
- An XP login-style title screen for “New Hire” with a “Clock in” action.
- A corporate desktop with authentic XP taskbar, Start menu, desktop icons, draggable/focusable/minimizable app windows, fake workday clock, energy indicator, and mute control.
- Always-visible Career Progress and Energy bars plus a “Today’s Priorities” note.
- Three playable work apps:
  - Documents: sort loose files into Finance, HR, and Misc.
  - Sheets 2003: complete one-cell or red-row spreadsheet instructions.
  - Notepad: accurately type corporate copy.
- A Break Room app that restores energy and exposes the player to boss interruptions.
- Three boss stages with increasing pressure: Squads messages, calls, and the VP sneak-up reflection.
- Promotion prompts and lightweight comic-style fallback scenes between bosses.
- Sleepy effects, energy failure, XP-style blue-screen game over, restart, final CEO victory, and replay.
- A narrow-screen XP error dialog, keyboard focus states, and reduced-motion support.

## Corporate treatment
- Keep the Windows XP Luna visual language and Tahoma typography.
- Replace the pastoral desktop feel with a fluorescent office/cubicle wallpaper treatment.
- Use deadpan corporate jargon, plausible filenames, status messages, and fake internal tools.
- Avoid modern SaaS styling, glass effects, decorative gradients, or unrelated redesigns.

## Technical approach
- Recreate only the useful XP shell patterns in the current React/TanStack app rather than importing the legacy React 16 runtime wholesale.
- Keep game values in one Zustand store and tuning constants in one balance module.
- Use CSS animations for sleepy, shake, pulse, and reflection effects.
- Use local/styled media fallbacks so the complete loop works now; future MP4/audio assets can replace them without changing game flow.
- Preserve the single `/` game route and add complete page metadata.

## Verification
- Exercise title → desktop → tasks → promotion → later boss mechanics → victory.
- Verify energy recovery, failure/restart, window focus/minimize behavior, keyboard actions, and 1024px minimum-width handling.
- Check desktop and narrow viewport screenshots and confirm the preview reports no build/runtime errors.
