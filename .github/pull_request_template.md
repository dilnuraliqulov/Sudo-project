## Summary

<!-- What does this PR change, and why? Keep it to a few sentences. -->

Closes #<!-- issue number, or delete this line -->

**Requirements:** <!-- e.g. FR-03, NFR-04, or "n/a" -->

## Type of change

- [ ] Feature
- [ ] Bug fix
- [ ] Refactor / cleanup
- [ ] Docs / design
- [ ] DevOps / tooling

**Area:** <!-- backend / frontend / devops / design / tests -->

## How to test

<!-- Steps a reviewer can follow to see this working (endpoints to call, pages to open, accounts to use). -->

1.
2.

## Screenshots

<!-- For UI changes: before/after screenshots or a short recording. Delete if not applicable. -->

## Checklist

**General**
- [ ] `make test` passes (or `pytest` from the repo root and `npm run check` in `frontend/`)
- [ ] Tests added or updated for new behavior
- [ ] No secrets, `.env` files, or `event_manager.db` committed
- [ ] Docs updated if behavior or setup changed (`README.md`, `CLAUDE.md`, `design/`)

**Backend** (delete if untouched)
- [ ] Routes stay thin; business rules and ownership checks live in `services/`
- [ ] SQLAlchemy 2.0 style (`select()`, `Mapped[...]`), no `db.query()`
- [ ] Request bodies subclass `InputModel`, responses subclass `APIModel`, every route sets `response_model`
- [ ] Errors use the agreed status codes with a readable `detail` (400 / 401 / 403 / 404 / 409)
- [ ] Datetimes are timezone-aware (UTC)
- [ ] New settings added to both `Settings` and `.env.example`
- [ ] Model changes noted below (devs must delete `event_manager.db` and restart)

**Frontend** (delete if untouched)
- [ ] Handles loading, empty, and error states (shows `detail` from the API)
- [ ] 401 responses clear the token and redirect to login
- [ ] Checked at mobile width

## Notes for reviewers

<!-- Schema changes, follow-up work, open questions, anything risky. -->
