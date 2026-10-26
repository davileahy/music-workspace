# MVP Specification

## Goal

The goal of the MVP is to validate the core vision of **Music Workspace**.

By the end of the MVP, users should be able to organize, study and play music using a single application, replacing the need to switch between multiple websites, PDFs and note-taking apps.

The MVP prioritizes usability, simplicity and organization over feature quantity.

---

# Core Experience

The MVP should allow users to:

- Browse a small public music library.
- Search and open songs.
- View lyrics, chords and chord diagrams.
- Create and manage a personal music library.
- Import existing chord sheets.
- Create playlists.
- Take personal notes.
- Practice songs without unnecessary distractions.

---

# Features

## Authentication

Users have a personal workspace.

### Requirements

- Register an account.
- Log in.
- Log out.

### Out of Scope

- Social login.
- Password recovery.
- Multi-factor authentication.

---

## Public Library

A small public library demonstrates the application's capabilities.

The initial catalog is intended for validation only and does not aim to be comprehensive.

### Requirements

- Browse songs.
- Search by title.
- Search by artist.
- Open a song page.

### Out of Scope

- Community editing.
- Ratings.
- Comments.
- Song versions.
- Large music catalog.

---

## Music Page

Every song has a dedicated page.

### Required Information

- Title
- Artist
- Key
- Lyrics
- Chords
- Chord diagrams
- Capo
- Tuning

### Optional

- Tabs

### Out of Scope

- Comments.
- Version history.
- Community discussions.
- Difficulty rating.

---

## My Library

Users can maintain their own private music collection.

### Requirements

- Create songs.
- Edit songs.
- Delete songs.
- Organize personal songs.
- Save imported songs.

All content is private by default.

---

## Import

Users can import existing chord sheets into their personal library.

### Requirements

- Import PDF.
- Import image.
- Import plain text.
- Extract text from imported documents.
- Allow users to review and edit extracted content before saving.

### Out of Scope

- Automatic song generation.
- AI-assisted formatting.
- OCR for complex handwritten documents.

---

## Notes

Users can create private notes associated with songs.

### Requirements

- Create notes.
- Edit notes.
- Delete notes.

### Out of Scope

- Audio notes.
- Shared notes.

---

## Chord Diagrams

The application displays chord diagrams while viewing songs.

### Requirements

- Guitar support.
- Acoustic guitar support.
- Display chord diagrams.
- Browse chord variations.

### Out of Scope

- Piano.
- Ukulele.
- Other instruments.

---

## Playlists

Users can organize songs into playlists.

### Requirements

- Create playlists.
- Rename playlists.
- Delete playlists.
- Add songs.
- Remove songs.
- Reorder songs.

---

## Workspace

The workspace provides a distraction-free environment for studying and playing music.

### Requirements

- Clean reading interface.
- Responsive layout.
- Playlist navigation.
- Fullscreen support.

### Out of Scope

- Auto-scroll.
- Metronome.
- Tuner.

---

## Search

### Requirements

- Search by title.
- Search by artist.
- Fast and responsive results.

### Out of Scope

- Filters.
- Search history.
- Recommendations.

---

# Out of Scope

The following features are intentionally excluded from the MVP:

- Community editing.
- Reputation system.
- Public user profiles.
- Comments.
- Ratings.
- Version history.
- AI-assisted editing.
- Chord detection through microphone.
- Scale explorer.
- Related chords.
- Piano support.
- Additional instruments.
- Mobile application.
- Recommendation system.
- Music streaming.
- Audio recording.

---

# Definition of Done

The MVP is considered complete when a user can:

- Create an account.
- Log in.
- Browse the public music library.
- Search and open songs.
- View chord diagrams.
- Create and manage a private music library.
- Import and review personal chord sheets.
- Create playlists.
- Take private notes.
- Practice songs using a clean, distraction-free interface.

At this point, Music Workspace successfully validates its core value proposition as a personal music workspace.