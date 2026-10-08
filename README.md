# 🌊 Marine Safety & Environmental Support Mobile App
> **Coursework Project: UI/UX Design & Cloud Architecture (Azure)**

## 🔄 App Workflow & User Journey


```mermaid
graph TD
    Start([App Launch]) --> Login[Login Screen]
    Login --> RoleSelect{Role Selection}

    RoleSelect -->|"Diver"| DiverDash[Diver Dashboard]
    RoleSelect -->|"Swimmer"| SwimmerDash[Swimmer Dashboard]
    RoleSelect -->|"Fisher"| FisherDash[Fisher Dashboard]
    RoleSelect -->|"Sailor"| SailorDash[Sailor Dashboard]

    DiverDash --> DiverFeat["• Oxygen Tank Level<br/>• Health Measures"]
    FisherDash --> FisherFeat["• Fish Species Detection<br/>• GPS Tracking & Radar"]
    SailorDash --> SailorFeat["• Weather Warnings<br/>• Wearable Device Sync"]

    subgraph Core ["Environmental & Community Features"]
        Camera["Capture Marine Debris"] --> Gallery["App Gallery Storage"]
        Gallery --> SendAuth["Submit to Marine Authorities"]
        SendAuth --> Status["Status: Reported"]
        
        Emergency["AI Emergency Alert"] --> Outsider["Marine Animal Alarm Sound"]
        TeamShare["Share Location with Team"]
    end

    DiverDash -.-> Camera
    SwimmerDash -.-> Camera
    FisherDash -.-> Camera
    SailorDash -.-> Camera

    Status --> End([Completed])

Figma Screen Breakdown (UI/UX Prototype)

Trang 1: Màn hình Đăng nhập & Chọn vai trò (Role Selection Login) - Có logo ứng dụng và 4 nút chọn rõ ràng tương ứng với: Diver, Swimmer, Fisher, Sailor.

Trang 2: Màn hình Dashboard dành cho Thợ lặn (Diver Dashboard) - Hiển thị các chỉ số trực quan như mức bình dưỡng khí, nhịp tim, huyết áp.

Trang 3: Màn hình dành cho Ngư dân (Fisher Radar & Tracking) - Hiển thị tính năng định vị loài cá xung quanh và theo dõi tọa độ vị trí GPS & Radar.

Trang 4: Màn hình Báo cáo rác thải biển (Marine Debris Capture) - Giao diện camera có nút chụp ảnh rác thải nhựa/ô nhiễm trôi nổi trên biển.

Trang 5: Thư viện ảnh và Trạng thái gửi báo cáo (Gallery & Status) - Hiển thị danh sách các bức ảnh rác đã chụp dưới dạng lưới, kèm trạng thái báo cáo Reported.

Trang 6: Màn hình Cảnh báo nguy hiểm & Thời tiết (Weather & Emergency) - Hiển thị cảnh báo bão trước khi ra khơi, nút kích hoạt còi báo động sinh vật biển và kết nối thiết bị đeo.
