# System Design

```mermaid
flowchart TD
  UI[Next.js UI] --> Game[Balance Scale Feature]
  Game --> Content[Versioned Challenge JSON]
  Game --> Engine[Challenge Validator]
  Game --> Voice[Browser Speech Synthesis]
  Game --> Progress[Local Progress Storage]
  UI --> Vercel[Vercel Deployment]
```

## Ranh giới
UI không chứa trực tiếp quy tắc kiểm tra bài; tách thành engine thuần để unit test. Audio phụ thuộc khả năng trình duyệt và có fallback văn bản.
