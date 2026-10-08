# 🌊 Marine Safety & Environmental Support Mobile App
> **Coursework Project: UI/UX Design & Cloud Architecture (Azure)**

## 🔄 App Workflow & User Journey


```mermaid
graph TD
    %% Khởi động ứng dụng
    Start([Mở ứng dụng]) --> Login[Màn hình Đăng nhập / Xác thực]
    Login --> RoleSelect{Lựa chọn vai trò người dùng}

    %% Phân rã theo vai trò
    RoleSelect -->|Diver (Thợ lặn)| DiverDash[Dashboard Thợ lặn]
    RoleSelect -->|Swimmer (Bơi lội)| SwimmerDash[Dashboard Bơi lội]
    RoleSelect -->|Fisher (Ngư dân)| FisherDash[Dashboard Ngư dân]
    RoleSelect -->|Sailor (Thủy thủ)| SailorDash[Dashboard Thủy thủ]

    %% Tính năng đặc thù theo vai trò
    DiverDash --> DiverFeat[• Kiểm tra mức bình oxy <br/>• Chỉ số sinh trắc học: Nhịp tim, Huyết áp]
    FisherDash --> FisherFeat[• Định vị loài cá xung quanh <br/>• Tracking vị trí GPS & Radar]
    SailorDash --> SailorFeat[• Cảnh báo thời tiết trước khi ra khơi <br/>• Kết nối thiết bị đeo Wearables]

    %% Tính năng chung (Core Features)
    subgraph Core_Features [Tính năng cốt lõi & Môi trường]
        Camera[Chụp ảnh rác thải / Ô nhiễm nhựa biển] --> Gallery[Lưu trữ vào thư viện App Gallery]
        Gallery --> SendAuth[Gửi báo cáo đến Cơ quan Hải quan / Môi trường]
        SendAuth --> Status[Cập nhật trạng thái: 'Submitted / Reported']
        
        Emergency[Hệ thống khẩn cấp AI & Còi báo động] --> Outsider[Cảnh báo sinh vật biển nguy hiểm cho bên ngoài]
        TeamShare[Chia sẻ hình ảnh & Vị trí với đồng đội]
    end

    %% Liên kết các vai trò với tính năng chung
    DiverDash -.-> Camera
    SwimmerDash -.-> Camera
    FisherDash -.-> Camera
    SailorDash -.-> Camera

    %% Kết thúc luồng
    Status --> End([Hoàn tất quy trình báo cáo])
