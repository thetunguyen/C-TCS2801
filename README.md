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
