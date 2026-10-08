# 🌊 Marine Safety & Environmental Support Mobile App
> **Coursework Project: UI/UX Design & Cloud Architecture (Azure)**

## 🔄 App Workflow & User Journey


```mermaid
graph TD
    Start([Mở ứng dụng]) --> Login[Màn hình Đăng nhập]
    Login --> RoleSelect{Lựa chọn vai trò}

    RoleSelect -->|"Diver (Thợ lặn)"| DiverDash[Dashboard Thợ lặn]
    RoleSelect -->|"Swimmer (Bơi lội)"| SwimmerDash[Dashboard Bơi lội]
    RoleSelect -->|"Fisher (Ngư dân)"| FisherDash[Dashboard Ngư dân]
    RoleSelect -->|"Sailor (Thủy thủ)"| SailorDash[Dashboard Thủy thủ]

    DiverDash --> DiverFeat["• Kiểm tra bình oxy<br/>• Chỉ số sinh trắc học"]
    FisherDash --> FisherFeat["• Định vị loài cá<br/>• Tracking GPS & Radar"]
    SailorDash --> SailorFeat["• Cảnh báo thời tiết<br/>• Kết nối thiết bị đeo"]

    subgraph Core ["Tính năng Môi trường & Cộng đồng"]
        Camera["Chụp ảnh rác thải nhựa"] --> Gallery["Lưu trữ App Gallery"]
        Gallery --> SendAuth["Gửi báo cáo Hải quan"]
        SendAuth --> Status["Trạng thái: Reported"]
        
        Emergency["Cảnh báo khẩn cấp AI"] --> Outsider["Còi báo động sinh vật biển"]
        TeamShare["Chia sẻ vị trí với đồng đội"]
    end

    DiverDash -.-> Camera
    SwimmerDash -.-> Camera
    FisherDash -.-> Camera
    SailorDash -.-> Camera

    Status --> End([Hoàn tất])
