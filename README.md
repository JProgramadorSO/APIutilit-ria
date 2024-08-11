# API utilitária
API utilitária que oferece dados úteis sobre antirracismo, desmatamento na Amazônia e mudanças climáticas.


Código:
Código em JavaScript (Node.js com Express)

const express = require('express');
const app = express();
const port = 3000;

// Lista de livros sobre antirracismo
const antiRacismBooks = [
 { title: "How to Be an Antiracist", author: "Ibram X. Kendi" },
 { title: "White Fragility", author: "Robin DiAngelo" },
 { title: "The New Jim Crow", author: "Michelle Alexander" },
 // Adicione mais livros conforme necessário
];

// Dados fictícios sobre desmatamento na Amazônia
const amazonDeforestationData = {
 year: 2023,
 area_deforested: "10,000 km²",
 primary_causes: ["Agriculture", "Illegal logging", "Fires"]
};

// Dados fictícios sobre mudanças climáticas
const climateChangeData = {
 year: 2023,
 global_temperature_increase: "1.2°C",
 major_contributors: ["CO2 emissions", "Deforestation", "Industrial activity"]
};

// Rota para obter livros sobre antirracismo
app.get('/books/anti-racism', (req, res) => {
 res.json(antiRacismBooks);
});

// Rota para obter dados sobre desmatamento na Amazônia
app.get('/data/amazon-deforestation', (req, res) => {
 res.json(amazonDeforestationData);
});

// Rota para obter dados sobre mudanças climáticas
app.get('/data/climate-change', (req, res) => {
 res.json(climateChangeData);
});

app.listen(port, () => {
 console.log(`API listening at http://localhost:${port}`);
});
