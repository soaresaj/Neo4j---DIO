// =============================================
// **CONSULTAS E ESTATÍSTICAS**
// =============================================

// ***1 Estatística geral***
MATCH (n) RETURN 'Nós' AS tipo, count(n) AS total
UNION ALL
MATCH ()-[r]->() RETURN 'Relacionamentos' AS tipo, count(r) AS total;
Resposta:
╒═════════════════╤═════╕
│tipo             │total│
╞═════════════════╪═════╡
│"Nós"            │381  │
├─────────────────┼─────┤
│"Relacionamentos"│1889 │
└─────────────────┴─────┘
