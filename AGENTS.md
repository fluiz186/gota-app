<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Water duel: XP is derived client-side from `drinks` rows (src/lib/xp.ts), never stored — keeps rules changeable in one place.
- Days are bucketed in America/Sao_Paulo (`drinks.day` default + `todaySP()`) so both players share the same day.
- Avatar equipment is stored on each user's profile; unlock eligibility is derived from that user's lifetime `drinks` rows, not client-supplied milestones — preserves existing XP logic and prevents equipped locked items from rendering.
