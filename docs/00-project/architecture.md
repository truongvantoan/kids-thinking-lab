# Architecture Overview

- Frontend: Next.js App Router + React + TypeScript.
- Game UI: feature modules; shared UI components.
- Domain: challenge schema, validators, level progression, mastery policies.
- Content: versioned JSON, reviewable in GitHub.
- MVP persistence: localStorage (không đồng bộ đa thiết bị).
- Future: API + database cho phụ huynh, tiến độ, content versioning.
- Deployment: GitHub main → Vercel production; PR → preview.

## Security
Không lưu giọng nói trẻ em trên server khi chưa có thiết kế consent, retention và deletion rõ ràng.
