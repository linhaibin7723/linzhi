# OCAT-style response UI changes

- AI response now starts directly with the most natural spoken translation.
- Prompt enforces this learning order: translation -> sentence analysis -> usage -> key vocabulary -> examples -> natural expressions -> common replies -> practice.
- Every complete target-language sentence is marked internally with `[SENTENCE]...[/SENTENCE]` and rendered as an independent interactive sentence card.
- Each sentence card has direct play and sentence-level bookmark actions.
- Sentence bookmarks are persisted in the existing SQLite bookmark table and therefore appear in the existing collection/bookmark screen.
- Streaming partial sentence markers are rendered without exposing protocol tags.
- Ordinary explanation lines and section headings use a cleaner OCAT-like card layout instead of the old dense Markdown rendering.

Build verification note: the local environment could not download the Gradle 9.5 distribution because outbound network access is unavailable, so a full Gradle compile/test could not be executed here.
