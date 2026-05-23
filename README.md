    graph TD
    A((Start:<br/>Thai Syllable)) --> B(Mid Consonants<br/>อักษรกลาง)
    A --> C(High Consonants<br/>อักษรสูง)
    A --> D(Low Consonants<br/>อักษรต่ำ)

    %% Mid Consonants
    B --> B1{Tone Mark?}
    B1 -->|None| B2{Syllable Type}
    B2 -->|Live| B_Mid[Mid Tone  - ]:::mid
    B2 -->|Dead| B_Low[Low Tone  ˋ ]:::low
    B1 -->|Mai Ek ่| B_Low2[Low Tone  ˋ ]:::low
    B1 -->|Mai Tho ้| B_Fall[Falling Tone  ˆ ]:::fall
    B1 -->|Mai Tri ๊| B_High[High Tone  ˊ ]:::high
    B1 -->|Mai Chattawa ๋| B_Rise[Rising Tone  ˇ ]:::rise

    %% High Consonants
    C --> C1{Tone Mark?}
    C1 -->|None| C2{Syllable Type}
    C2 -->|Live| C_Rise[Rising Tone  ˇ ]:::rise
    C2 -->|Dead| C_Low[Low Tone  ˋ ]:::low
    C1 -->|Mai Ek ่| C_Low2[Low Tone  ˋ ]:::low
    C1 -->|Mai Tho ้| C_Fall[Falling Tone  ˆ ]:::fall
    
    %% Low Consonants
    D --> D1{Tone Mark?}
    D1 -->|None| D2{Syllable Type}
    D2 -->|Live| D_Mid[Mid Tone  - ]:::mid
    D2 -->|Dead| D3{Vowel Length}
    D3 -->|Short| D_High[High Tone  ˊ ]:::high
    D3 -->|Long| D_Fall[Falling Tone  ˆ ]:::fall
    D1 -->|Mai Ek ่| D_Fall2[Falling Tone  ˆ ]:::fall
    D1 -->|Mai Tho ้| D_High2[High Tone  ˊ ]:::high

    %% ပြတ်သားပြီး ကြည့်ရအဆင်ပြေမယ့် Color Design များ
    classDef mid fill:#E3F2FD,stroke:#1E88E5,stroke-width:2px,color:#0D47A1;
    classDef low fill:#FFF3E0,stroke:#FB8C00,stroke-width:2px,color:#E65100;
    classDef fall fill:#FFEBEE,stroke:#E53935,stroke-width:2px,color:#B71C1C;
    classDef high fill:#F3E5F5,stroke:#8E24AA,stroke-width:2px,color:#4A148C;
    classDef rise fill:#E8F5E9,stroke:#4CAF50,stroke-width:2px,color:#1B5E20;
