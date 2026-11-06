# Data Model (Draft)

```ts
type Difficulty = 'D1'|'D2'|'D3'|'D4'|'D5';
type Challenge = {id:string; epicId:string; levelId:string; difficulty:Difficulty; prompt:string; scene:unknown; options:{id:string;image:string;label:string}[]; correctOptionId:string; explanation:string; narration?:{intro?:string;question:string;feedback?:string}};
type Attempt = {challengeId:string; selectedOptionId:string; explained:boolean; correct:boolean; createdAt:string};
type Progress = {unlockedLevel:number; attempts:Attempt[]};
```

Tất cả ID ổn định qua các lần chỉnh sửa nội dung; migration khi thay schema.
