# DashboardPanel

Khối lớn của Dashboard (Việc, Lịch, Lịch trình): nền `container`, viền 1px `border`, bo `radius-xl`, lề trong 20px — container chuẩn của app, không phải card shadcn.

- Lớp: `dq-panel`; tiêu đề `dq-panel-head` gồm icon tile 28px (`dq-tile`), tên khối `dq-panel-title` 20px đậm 700, phụ đề `dq-panel-sub` cùng cỡ font-light màu muted, cuối là `dq-count`. Khe 10px.
- Khe giữa các thẻ trong khối 12px; giữa các khối 16px.
- Không thêm bóng. Không tô nền đỏ.
- Lưới Dashboard: `minmax(0,1fr) 340px 340px`, rời về một cột dưới 1280px.
