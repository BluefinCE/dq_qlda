# TaskCard

Thẻ việc bên trong một DashboardPanel (tầng 2 — inset): nền `background`, viền 1px, bo `radius-lg`, lề 16px.

- Lớp: `dq-task`; icon tile 44px `dq-task-icon` lấy nền từ tone lịch (`dq-bg-sky|violet|amber|pink|emerald`); tiêu đề `dq-task-title` 14px đậm 600; meta 12px muted kèm `dq-status` và `dq-chip`.
- Hover: nền `accent` 40%.
- **Quá hạn** (`dq-task-overdue`): viền `overdue-border` + vòng sáng nhấp nháy 5s chạy trên box-shadow (spread tối đa 4px — không chạm thẻ kề, khe 12px). `prefers-reduced-motion`: viền tĩnh 3px.
- Không dùng `transform: scale`.
