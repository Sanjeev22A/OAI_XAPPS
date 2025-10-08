```mermaid
graph TD
    %% Title
    A[F1 Application Protocol (F1AP) Modules]:::title

    %% CU Side
    subgraph B[CU-side]
        B1[f1ap_cu_task.c<br/>→ Processes F1AP messages]
        B2[f1ap_cu_interface_management.c<br/>→ Sets up F1 connection]
        B3[f1ap_cu_ue_context_management.c<br/>→ Manages UE context]
        B4[f1ap_cu_rrc_message_transfer.c<br/>→ Transfers RRC messages]
        B5[f1ap_cu_paging.c<br/>→ Handles paging]
    end

    %% DU Side
    subgraph C[DU-side]
        C1[f1ap_du_task.c<br/>→ Processes F1AP messages]
        C2[f1ap_du_interface_management.c<br/>→ Manages F1 connection]
        C3[f1ap_du_ue_context_management.c<br/>→ Manages UE context]
        C4[f1ap_du_rrc_message_transfer.c<br/>→ Transfers RRC messages]
        C5[f1ap_du_paging.c<br/>→ Handles paging]
    end

    %% Shared/Common Components
    subgraph D[Shared / Common]
        D1[f1ap_common.c<br/>→ Common utilities]
        D2[f1ap_encoder.c<br/>→ Message encoding/decoding]
        D3[f1ap_ids.c<br/>→ ID management]
    end

    %% Connections
    B1 --> D1
    B2 --> D2
    B3 --> D3
    B4 --> D2
    B5 --> D1

    C1 --> D1
    C2 --> D2
    C3 --> D3
    C4 --> D2
    C5 --> D1

    %% Styling
    classDef title fill=#f5f5f5,stroke=#333,stroke-width=1.5px,font-weight:bold;
    classDef subgraphTitle fill=#eef,stroke=#888,stroke-width=1px;
    classDef default fill=#fff,stroke=#999,stroke-width=0.5px;

```
