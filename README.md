```mermaid
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

    %% Styling to make outputs pop
    classDef mid fill:#e0f7fa,stroke:#006064,stroke-width:2px;
    classDef low fill:#fff3e0,stroke:#e65100,stroke-width:2px;
    classDef fall fill:#ffebee,stroke:#b71c1c,stroke-width:2px;
    classDef high fill:#f3e5f5,stroke:#4a148c,stroke-width:2px;
    classDef rise fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px;
